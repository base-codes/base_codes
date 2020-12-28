<template>
  <div class="error-wrapper">
    <div class="error-block">
      <div class="columns">
        <div class="column is-offset-3">
          <h1 v-if="error.statusCode === 404" class="headler-error">
            404
          </h1>
          <h1 v-else>
            An error occurred
          </h1>
        </div>
      </div>
      <hr>
      <div class="columns">
        <div class="column is-3">
          <p>Error</p>
        </div>
        <div class="column is-6">
          <p>
            Unfortunately something went wrong. Please dubble check the URL or
            go back to the landing page. If you countinue to get this error -
            please email us at support@everydayexperiments.ikea.com
          </p>
        </div>
        <div class="column is-3">
          <div class="to-home">
            <p class="home-button" @click="toHome">
              Home page
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['error'],
  methods: {
    toHome () {
      this.$router.push('/')
    }
  }
}
</script>

<style lang="scss">
.error-wrapper {
  height: 100vh;
  padding: 0 64px;

  .error-block {
    height: 90%;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding-top: 88px;
  }
  .home-button {
    padding: 16px 64px;
    border: 1px solid white;
    display: inline;
    box-sizing: border-box;
    cursor: pointer;
  }
  .to-home {
    display: flex;
    justify-content: flex-end;
  }
  .headler-error {
    font-size: 256px;
  }
}
</style>
