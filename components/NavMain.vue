<template>
  <div class="header">
    <div class="logo">
      <p @click="openNav">
        BASE
      </p>
    </div>
    <nav :class="withVissible ? 'fadeIn':''" class="">
      <nuxt-link to="/">
        Home
      </nuxt-link>
      <nuxt-link to="/projects">
        Projects
      </nuxt-link>
      <nuxt-link to="/projects">
        About
      </nuxt-link>
      <nuxt-link to="/projects">
        Identy
      </nuxt-link>
      <nuxt-link to="/projects">
        illustration
      </nuxt-link>
      <nuxt-link to="/projects">
        Web
      </nuxt-link>
      <nuxt-link to="/projects">
        Content
      </nuxt-link>
    </nav>

    <div class="navButton">
      <span>Menu</span>
    </div>
  </div>
</template>

<style lang="scss">
    .navButton{
        position: absolute;
        top: 0;
        right: 0;
    }
    nav{
      width: 0;
    }
    .fadeIn{
        width: 100%;
        transition: width .3s ease-in;
    }

</style>
<script>
export default {
  data () {
    return {
      withVissible: false
    }
  },
  methods: {
    openNav () {
      this.withVissible = !this.withVissible
    }

  }

}
</script>
