<template>
    <div class="nav">
        <el-menu :default-active="activeIndex"
                 class="el-menu-nav"
                 mode="horizontal"
                 router="true"
                 text-color="#bde2d1"
                 active-text-color="#ffd04b"
                 collapse-transition="true"
                 @select="handleSelect">
          <el-menu-item index="/about">关于</el-menu-item>
          <el-submenu index="/life" >
            <template slot="title">我的日常</template>
            <el-menu-item index="/">运动</el-menu-item>
            <el-menu-item index="/">看书</el-menu-item>
            <el-menu-item index="/">电影</el-menu-item>
          </el-submenu>
          <el-menu-item index="##"><a href="#" >博客</a></el-menu-item>
          <el-menu-item index="#"><a href="#" >音乐播放器</a></el-menu-item>
        </el-menu>
    </div>
</template>

<script>
export default {
    name: "Nav",
    data() {
      return {
        activeIndex: '1',
      }
    },
    methods: {
      handleSelect(key, keyPath) {
          this.activeIndex = keyPath
        console.log(key, keyPath);
      }
    }
}
</script>

<style lang="scss" scoped>
  .nav {
    width: 100%;
  }
  .el-menu-nav {
     background-color: #f4f5f4;
  }


</style>
