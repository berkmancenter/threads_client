<template>
  <ContentHeader
    viewTitle="Create new thread"
    :contentTitle="topic.name"
    :color="appVariables.threadsColor"
  ></ContentHeader>

  <div class="new-thread-view p-5">
    <form @submit="createNewThread">
      <div class="field">
        <label class="label">Name</label>
        <div class="control">
          <input class="input" type="text" required v-model="threadName" ref="threadName" />
        </div>
      </div>

      <div class="field is-grouped">
        <div class="control">
          <button class="button is-success">Create</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import axios from 'axios'
import ContentHeader from '@/components/Shared/ContentHeader/Index'

export default {
  name: 'new-thread-index',
  components: {
    ContentHeader,
  },
  data() {
    return {
      threadName: '',
      topic: {},
    }
  },
  created() {
    this.loadTopic()
  },
  mounted() {
    this.$refs.threadName.focus()
  },
  computed: {},
  methods: {
    createNewThread(e) {
      e.preventDefault()

      axios
        .post(`${process.env.API_SERVER_URL}/v1/threads`, {
          name: this.threadName,
          topicId: this.topic.id,
        })
        .then((response) => {
          this.threadName = ''
          this.$router.push({ name: 'thread.index', params: { threadId: response.data.id } })
          this.$store.dispatch('user/reloadUserThreads')
        })
    },
    loadTopic() {
      axios
        .get(`${process.env.API_SERVER_URL}/v1/topics/${this.$route.params.topicId}`)
        .then((response) => {
          this.topic = response.data
        })
    },
  },
  watch: {
    '$route.params.topicId': function () {
      this.loadTopic()
    },
  },
}
</script>

<style lang="scss">
@import '@/assets/scss/Threads/NewThread/index.scss';
</style>
