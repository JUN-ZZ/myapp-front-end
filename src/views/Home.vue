<template>
  <div class="homeWrapper" >
    <el-container class="container"  >
      <el-header class="header">
        <Nav class="nav-head"></Nav>
      </el-header>
      <el-main class="main">
        <AppMain></AppMain>
      </el-main>
      <el-footer class="footer" style="height: 25px">
        <Footer></Footer>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
// @ is an alias to /src
import AppMain from "@/components/home/AppMain.vue";
import Nav from "@/components/nav/Nav";
import Footer from "./layout/Footer";

export default {
  name: 'Home',
  components: {
    AppMain,Nav,Footer
   },
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '0'
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }

}
</script>

<style lang="scss" scoped>

  .homeWrapper {
    width: 100%;
    height: 100%;
    position: absolute; /*设置了这个才能占满全屏 */
    top: 0;
    left: 0;
    padding: 0px;
    margin: 0px;
  }

  .container {
    width: 100%;
    height: 100%;
  }

  .header {
    width: 100%;
    height: 10%;
    line-height: 60px;
    padding: 0px;
  }

  .main {
    width: 100%;
    height: auto;
    text-align: center;
    line-height: normal;
    padding: 0px;

  }

  .footer {
    width: 100%;
    height: 5px;
    padding: 0px;
    background-color: rgba(228, 236, 227, 0.7);
  }


</style>
