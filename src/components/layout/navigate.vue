<template>
  <el-menu :default-active="activeIndex" class="menu-top" mode="horizontal" @select="handleSelect">
    <el-menu-item index="1">主页</el-menu-item>
    <el-menu-item index="2">人脉</el-menu-item>
    <el-menu-item index="3">职位</el-menu-item>
    <el-submenu index="4">
      <template slot="title">消息</template>
      <el-menu-item index="2-1">选项1</el-menu-item>
      <el-menu-item index="2-2">选项2</el-menu-item>
      <el-menu-item index="2-3">选项3</el-menu-item>
    </el-submenu>
    <el-menu-item index="4">发布职位</el-menu-item>
</el-menu>
</template>
<script>
export default {
  name: 'gnavigate',
  
}
</script>
<style>
  .g-navigate {
    position: absolute;
    padding: 10px;
    
    top: 60px;
    width: 200px;
    height: calc(100% - 60px);
    background: white;
    border-right: 1px solid rgba(0, 0, 0, .1);
  }

  .test {
    overflow: hidden;
  }
</style>