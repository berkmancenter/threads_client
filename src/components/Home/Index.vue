<template>
  <div class="home-view">
    <div class="has-text-centered">
      <h1 class="is-size-1">Hello Anon</h1>
      <h2 class="is-size-2">Talk <strong>Really</strong> Pseudonymously</h2>
    </div>

    <div class="has-text-centered my-4">
      <router-link class="button button-ok" :to="{ name: 'talk.index' }">
        <h2 class="is-size-2 has-text-weight-bold">Start</h2>
      </router-link>
    </div>

    <div class="home-view-who-we-are-banner home-view-background-base has-text-centered py-4">
      <div class="container px-2">
        <div class="is-flex is-flex-direction-column is-align-items-center p-4">
          <h4 class="is-size-4">Who We Are</h4>

          <h5 class="is-size-5">
            The Berkman Klein Center's mission is to explore and understand cyberspace; to study its
            development, dynamics, norms, and standards; and to assess the need or lack thereof for
            laws and sanctions.
          </h5>
          <h5 class="is-size-5">
            We are a research center, premised on the observation that what we seek to learn is not
            already recorded. Our method is to build out into cyberspace, record data as we go,
            self-study, and share. Our mode is entrepreneurial nonprofit.
          </h5>
        </div>
      </div>
    </div>

    <div class="columns">
      <div class="column">
        <div class="home-view-privacy has-text-centered">
          <div>
            <img alt="secure" src="@/assets/images/secure.png" />
          </div>
          <h4 class="is-size-4">We Will <strong>Never</strong> Sell Your Privacy</h4>
        </div>
      </div>
      <div class="column">
        <div class="home-view-track has-text-centered">
          <div>
            <img alt="track" src="@/assets/images/track.png" />
          </div>
          <h4 class="is-size-4">We Will <strong>Never</strong> Track You</h4>
        </div>
      </div>
    </div>

    <div class="home-view-trending home-view-background-base has-text-centered py-4">
      <div class="container px-2">
        <div class="columns is-4 p-4">
          <div class="column">
            <div>
              <h4 class="is-size-4">Trending Topics</h4>

              <ul>
                <li>Something cool</li>
                <li>Something cool</li>
                <li>Something cool</li>
                <li>Something cool</li>
                <li>Something cool</li>
              </ul>
            </div>
          </div>
          <div class="column">
            <div>
              <h4 class="is-size-4">Trending Threads</h4>

              <ul>
                <li>Something cool</li>
                <li>Something cool</li>
                <li>Something cool</li>
                <li>Something cool</li>
                <li>Something cool</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="home-view-noreg has-text-centered pt-4 pb-4">
      <div class="columns">
        <div class="column is-size-5">🟢 No registration</div>
        <div class="column is-size-5">📭 No emails</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home-index',
  components: {},
  data() {
    return {}
  },
  mounted() {},
  computed: {},
  methods: {},
}
</script>

<style lang="scss">
@import '@/assets/scss/Home/index.scss';
</style>
