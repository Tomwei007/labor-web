<template>
  <div class="main">
    <div class="header clearfix">
      <div class="header-title">
        <i class="el-icon-menu" @click="showMenu = !showMenu"></i>
        劳动力管理系统
      </div>
      <!--头部导航-->
      <div class="header-menu">
        <el-menu class="el-menu-demo" mode="horizontal" router background-color="#2138B2" active-text-color="#fff"
          text-color="#C6C6FF" :default-active="activeIndex">
          <el-menu-item index="/home">处理中心</el-menu-item>
          <el-submenu index="2" popper-class="header-submenu">
            <template slot="title">员工信息</template>
            <el-menu-item index="/info/user-info">
              用户信息
            </el-menu-item>
            <el-menu-item index="2-2" background-color="#fff">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
              <template slot="title">选项4</template>
              <el-menu-item index="2-4-1">选项1</el-menu-item>
              <el-menu-item index="2-4-2">选项2</el-menu-item>
              <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="3">考勤管理</el-menu-item>
          <el-menu-item index="4">行政排班</el-menu-item>
          <el-menu-item index="5">运营排班</el-menu-item>
          <el-menu-item index="6">放映排班</el-menu-item>
          <el-menu-item index="7">报表</el-menu-item>
        </el-menu>
      </div>
      <div class="header-con clearfix">
        <div class="con-message">
          <i class="el-icon-message-solid"></i>
        </div>
        <div class="con-setting">
          <i class="el-icon-setting"></i>
        </div>
        <div class="con-help">
          <i class="el-icon-question"></i>
        </div>
        <div class="con-user">
          <i class="el-icon-s-custom"></i>
          <span>张晓晓</span>
          <i class="el-icon-caret-bottom"></i>
        </div>
      </div>
    </div>
    <!--侧边导航-->
    <transition name="slide">
      <div class="aside-menu" v-if="showMenu">
        <el-menu router>
          <el-menu-item index="/home">处理中心</el-menu-item>
          <el-submenu index="2" popper-class="header-submenu">
            <template slot="title">员工信息</template>
            <el-menu-item index="/info/user-info">
              用户信息
            </el-menu-item>
            <el-menu-item index="2-2" background-color="#fff">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
              <template slot="title">选项4</template>
              <el-menu-item index="2-4-1">选项1</el-menu-item>
              <el-menu-item index="2-4-2">选项2</el-menu-item>
              <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="3">考勤管理</el-menu-item>
          <el-menu-item index="4">行政排班</el-menu-item>
          <el-menu-item index="5">运营排班</el-menu-item>
          <el-menu-item index="6">放映排班</el-menu-item>
          <el-menu-item index="7">报表</el-menu-item>
        </el-menu>
      </div>
    </transition>
    <div class="main-inner" @click="showMenu = false">
      <div class="main-breadcrumb">
        <el-breadcrumb separator-class="el-icon-arrow-right">
          <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
          <el-breadcrumb-item><a href="/">活动管理</a></el-breadcrumb-item>
          <el-breadcrumb-item>活动列表</el-breadcrumb-item>
          <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb>
      </div>
      <div class="main-content">
        <router-view />
      </div>
    </div>
  </div>

</template>

<script>
import './header.less'
export default {
  data () {
    return {
      activeIndex: '/home',
      showMenu: false
    }
  },
  methods: {
  }
}
</script>
