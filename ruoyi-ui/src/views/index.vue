<template>
  <div class="app-container home">
    <el-row :gutter="20">
      <el-col :span="24">
        <h1>系统菜单</h1>
        <el-divider />
      </el-col>
      
      <!-- 首页菜单 -->
      <el-col :xs="24" :sm="12" :md="8" :lg="6">
        <el-card class="menu-card">
          <div slot="header" class="clearfix">
            <span class="menu-title">
              <svg-icon icon-class="dashboard" />
              首页
            </span>
          </div>
          <el-menu router>
            <el-menu-item index="/">
              <span slot="title">首页</span>
            </el-menu-item>
          </el-menu>
        </el-card>
      </el-col>
      
      <!-- 系统管理菜单 -->
      <el-col :xs="24" :sm="12" :md="8" :lg="6">
        <el-card class="menu-card">
          <div slot="header" class="clearfix">
            <span class="menu-title">
              <svg-icon icon-class="system" />
              系统管理
            </span>
          </div>
          <el-menu router>
            <el-menu-item index="/system/user">
              <span slot="title">用户管理</span>
            </el-menu-item>
            <el-menu-item index="/system/role">
              <span slot="title">角色管理</span>
            </el-menu-item>
            <el-menu-item index="/system/menu">
              <span slot="title">菜单管理</span>
            </el-menu-item>
            <el-menu-item index="/system/dept">
              <span slot="title">部门管理</span>
            </el-menu-item>
            <el-menu-item index="/system/post">
              <span slot="title">岗位管理</span>
            </el-menu-item>
            <el-menu-item index="/system/dict">
              <span slot="title">字典管理</span>
            </el-menu-item>
            <el-menu-item index="/system/config">
              <span slot="title">配置管理</span>
            </el-menu-item>
            <el-menu-item index="/system/notice">
              <span slot="title">通知管理</span>
            </el-menu-item>
          </el-menu>
        </el-card>
      </el-col>
      
      <!-- 个人中心菜单 -->
      <el-col :xs="24" :sm="12" :md="8" :lg="6">
        <el-card class="menu-card">
          <div slot="header" class="clearfix">
            <span class="menu-title">
              <svg-icon icon-class="user" />
              个人中心
            </span>
          </div>
          <el-menu router>
            <el-menu-item index="/user/profile">
              <span slot="title">查看用户信息</span>
            </el-menu-item>
          </el-menu>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Index'
}
</script>

<style scoped>
.home {
  padding: 20px;
}

.menu-card {
  margin-bottom: 20px;
}

.menu-title {
  font-size: 16px;
  font-weight: bold;
}

.el-menu {
  border: none;
}

.el-menu-item {
  height: 40px;
  line-height: 40px;
}
</style>