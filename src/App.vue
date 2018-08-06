<template>
  <div id="app">
    <pj-header class="header"></pj-header>
    <div class="container">
      <pj-menu ref="lefeMenu"></pj-menu>
      <div class="right-bar">
        <div class="content">
            <router-view></router-view>
        </div>
        <pj-footer></pj-footer>
      </div>
      
    </div>
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
  height: 100%;
  background-color: #eee !important;
  margin: 0;
  padding: 0;
}
#app {
  height: 100%;
}
a{
  text-decoration: none;
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
  background-color: #777;
}

*::placeholder {
  font-size: 12px;
}

.container {
  display: flex;
  width: 1366px;
  height: 100%;
  // height: calc(100% - 46px);
  margin: auto;
  & .right-bar{
    width: 1136px;
    height: calc(100% - 120px);
    margin-left: 230px;
    position: fixed;
    & .content{
      min-height: calc(100% - 20px);
      padding: 20px 35px;
      background-color: #fff;
    }
  }

}

</style>
