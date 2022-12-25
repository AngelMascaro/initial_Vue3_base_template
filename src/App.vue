<template>
  <nav>
    <router-link to="/">{{$t('app.nav_link_home')}}</router-link> |
    <router-link to="/about">{{$t('app.nav_link_about')}}</router-link>
  </nav>
  <LanguageSwitcher class="LanguageSwitcher justify-content-start "/>
  <router-view/>
</template>

<script>
// import axios from "axios";
import LanguageSwitcher from "./components/LanguageSwitcher.vue"

export default {
  name: "App",
  components: {
    LanguageSwitcher
  },
    data(){
        return{
            user: {},
        }
    },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.LanguageSwitcher{
  position: absolute;
  right: 10px;
  top: 10px;
}
</style>
