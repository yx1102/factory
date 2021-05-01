<template>
  <div>
     <header class="defaultHeader">
      <h1 class="title">宏远坚华美建筑室</h1>
      <!-- 头部 -->
      <el-menu
        :default-active="$route.path"
        class="menu"
        mode="horizontal"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
        :router="true"
      >
        <el-menu-item :index="item.path" v-for="item in menuData" :key="item.title">
          <i :class="item.icon"></i>
          <span slot="title">{{item.title}}</span>
        </el-menu-item>
      </el-menu>
    </header>
  </div>
</template>

<script>
export default {
  name:'',
  data () {
    return {
       menuData: [
        {
          icon: 'el-icon-s-opportunity',
          title: '首页',
          path: '/'
        },
        {
          icon: 'el-icon-setting',
          title: '服务',
          path: '/service'
        },
        {
          icon: 'el-icon-phone',
          title: '联系',
          path: '/contact'
        },
      ],
    };
  },
}

</script>
<style lang='less' scoped>
.defaultHeader{
  width: 100%;
  height: 61px;
  background-color: #545c64;
  position: fixed;
  z-index: 9;
}

.title{
  width: 300px;
  height: 100%;
  line-height: 61px;
  color: #fff;
  display: inline-block;
  text-align: center;
  vertical-align: top;
}
.menu{
  width: calc(100% - 350px);
  display: inline-block;
}
</style>
