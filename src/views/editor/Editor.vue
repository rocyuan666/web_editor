<template>
  <div class="editor">
    <TopBar :height="40" />
    <div class="main-box">
      <LeftSidebar />
      <ContentMain />
      <RightSideBar />
    </div>
  </div>
</template>

<script setup name="Editor">
import LeftSidebar from './components/LeftSideBar/LeftSidebar.vue'
import RightSideBar from './components/RightSideBar/RightSideBar.vue'
import ContentMain from './components/ContentMain/ContentMain.vue'
import TopBar from './components/TopBar/TopBar.vue'
</script>

<style lang="scss" scoped>
.main-box {
  display: flex;
  background: #eee;
  .left-side-bar,
  .right-side-bar {
    width: 260px;
    background: #000;
  }
  .content-main {
    width: calc(100% - 520px);
    height: calc(100vh - 40px);
  }
}
</style>
