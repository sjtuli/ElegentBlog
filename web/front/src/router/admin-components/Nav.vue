<template>
  <!-- 左侧导航栏 -->
  <el-menu mode="vertical" @select="goToPage">
    <el-menu-item index="admin/login">
      <el-icon>
        <House />
      </el-icon>
      <span>仪表盘</span>
    </el-menu-item>
    <el-sub-menu>
      <template #title>
        <el-icon>
          <MessageBox />
        </el-icon>
        <span>文章管理</span>
      </template>
      <el-menu-item index="admin/article/AddArt">
        <el-icon>
          <Edit />
        </el-icon>
        <span>写文章</span>
      </el-menu-item>
      <el-menu-item index="admin/article/ArtList">
        <el-icon>
          <Document />
        </el-icon>
        <span>文章列表</span>
      </el-menu-item>
    </el-sub-menu>

    <el-menu-item index="admin/comment">
      <el-icon>
        <ChatLineRound />
      </el-icon>
      <span>评论管理</span>
    </el-menu-item>
    <el-menu-item index="admin/category">
      <el-icon>
        <Files />
      </el-icon>
      <span>分类列表</span>
    </el-menu-item>

    <el-menu-item index="admin/userlist">
      <el-icon>
        <User />
      </el-icon>
      <span>用户列表</span>
    </el-menu-item>

    <el-menu-item index="admin/profile">
      <el-icon>
        <Setting />
      </el-icon>
      <span>个人设置</span>
    </el-menu-item>
  </el-menu>
</template>

<script setup lang="ts">
  import router from '/@/router';

  const goToPage = (key: string, keyPath: string[]) => {
    console.log(key, keyPath);
    router.push('/' + key).catch((err) => err);
  };
</script>

<style scoped>
  .log {
    height: 32px;
    margin: 16px;
    background-color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 17px;
  }
</style>
