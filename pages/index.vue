<template>
  <div>
    <carousel />

    <!-- 关于我们 -->
    <div class="about">
      <el-divider><i class="el-icon-s-open"></i></el-divider>
      <div class="left">
        <img src="../assets/images/1.jpg" alt="" />
      </div>
      <div class="right">
        <div class="header">
          <p class="title">关于我们</p>
          <p class="subTitle">ABOUT US</p>
        </div>
        <div class="content">
          <span>
            我们是广州宏远坚华美建筑室内外服务一站式有限公司，一家全面服务的设计和咨询公司，业务范围包括规划与景观设计所、市政与设备设计所，有些建筑设计院还设立分院，专业范围包括城市规划、建筑工程设计、景观设计、室内设计、市政设计、消防设计、智能设计等，业务涉及中外合作设计，施工图设计审查，工程承包，环境艺术，建筑智能化工程等。
          </span>
        </div>
      </div>
    </div>

    <!-- 精选案例 -->
    <div class="project">
    <el-divider><i class="el-icon-connection"></i></el-divider>
      <div class="header">
        <p class="title">精选案例</p>
        <p class="subTitle">PROJECT</p>
      </div>
      <div class="content">
        <el-card class="box-card" v-for="item in srcList" :key="item">
          <el-image :src="item">
            <div slot="placeholder" class="image-slot">
              加载中<span class="dot">...</span>
            </div>
          </el-image>
        </el-card>
      </div>
    </div>
  </div>
</template>

<script>
import carousel from "../components/carousel";
export default {
  name: "",
  components: {
    carousel
  },
  data() {
    return {
      srcList: [
        require("../assets/images/3.jpg"),
        require("../assets/images/4.jpg"),
        require("../assets/images/5.jpg"),
        require("../assets/images/6.jpg"),
        require("../assets/images/7.jpg"),
        require("../assets/images/8.jpg")
      ]
    };
  }
};
</script>
<style lang="less" scoped>
.about {
  margin: 30px;
  margin-top: 80px;
  .left {
    display: inline-block;
  }
  .right {
    display: inline-block;
    vertical-align: top;
    text-align: center;
    width: calc(100% - 500px - 60px);
    .header {
      height: 150px;
      line-height: 50px;
      .title {
        font-size: 26px;
        font-weight: 600;
      }
    }
  }
}
.project {
  margin-top: 100px;
  text-align: center;
  .header {
    .title {
      font-size: 26px;
      font-weight: 600;
    }
  }
  .content {
    .box-card {
      width: 400px;
      margin-top: 50px;
      margin-left: 40px;
      display: inline-block;
    }
  }
}
</style>
