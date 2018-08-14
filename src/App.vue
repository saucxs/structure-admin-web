<template>
  <div id="app">
    <pj-header class="header"></pj-header>
    <div class="container">
      <div class="content">
        <router-view></router-view>
      </div>
    </div>
    <!-- <pj-footer></pj-footer> -->
    <pj-menu ref="lefeMenu" class="left-menu"></pj-menu>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";
import pjHeader from './components/header'
import pjMenu from "./components/menu";
import pjFooter from "./components/footer";
export default {
  data() {
    return {
      
    }
  },
  components: {
    pjHeader,
    pjMenu,
    pjFooter
  }
}
</script>

<style lang="postcss">
body {
  width: 100%;
  height: 100%;
  background-color: #eee !important;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
#app {
  height: 100%;
}
a {
  text-decoration: none;
  color: #000;
}
a:focus,a:active{
  color: #000;
}

*::-webkit-scrollbar {
  width: 5px;
  height: 5px;
}

*::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  background-color: #f5f5f5;
}

*::-webkit-scrollbar-thumb {
  border-radius: 10px;
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  background-color: #409eff;
}

*::placeholder {
  font-size: 12px;
}

.header{
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
  width: 100%;
  height: 60px;
}

.container {
    position: fixed;
    top: 46px;
    left: 190px;
    padding: 10px 20px;
    background: #fff;
    height: calc(100% - 20px);
    width: calc(100% - 230px);
    overflow: auto;
    & .content{
      margin-bottom: 60px;
    }
}

.left-menu{
  position: fixed;
  left: 0;
  top: 46px;
  width: 180px;
  height: 100%;
}

</style>
