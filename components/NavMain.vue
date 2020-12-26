<template>
  <div class="header">
    <div class="logo">
      <p>
        base
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

    <div class="navButton" @click="openNav">
      <span :class="withVissible ? 'hideMenu':''" class="btnMenu">Menu</span>
      <span :class="withVissible ? '':'hideX'" class="btnMenu">X</span>
    </div>
  </div>
</template>

<style lang="scss">
    .header{
      display: flex;
      justify-content: space-between;
      padding: 32px 64px;
      background-color: #000;
    }
    .navButton{
      color: #fff;
      cursor: pointer;
      width: 6%;
      position: relative;
      overflow: hidden;
      &:hover{
      }
    }
    .hideMenu{
      top: -110% !important;
    }
    .hideX{
      top: 110% !important;
    }
    .btnMenu{
      display: flex;
      justify-content: center;
      width: 100%;
      position: absolute;
      right: 0;
      top: 0;
      transition: .4s ease-in-out;
    }
    .logo{
      padding: 0px 15px;
      background-color: #fff;
      color: #000;
      z-index: 10;
    }
    nav{
      width: 0%;
      position: fixed;
      top: 0;
      right: 0;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
      background-color: #000;
      font-size: 48px;
      font-weight: 400;
      transition: width .4s ease-in-out;
      a:nth-child(1){
        margin-top: 100px;
      }
      a:nth-child(7){
        margin-bottom: 100px;
      }
      a{
        color: #606060;
        margin-left: 64px;
      }
      a:hover::before{
        content: "//";
      }
      a:hover{
        color: #fff;
      }

    }
    .fadeIn{
        width: 100%;
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
