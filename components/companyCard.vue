<template>
  <div class="company">
    <el-card
      :body-style="{ padding: '0px' }"
      v-for="item in cardList"
      :key="item.desc"
      class="card"
    >
      <img :src="item.img" class="image" />
      <div style="padding: 14px;">
        <span>{{ item.title }}</span>
        <div class="bottom clearfix">
          <time class="time">{{ item.desc }}</time>
        </div>
      </div>
    </el-card>
  </div>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      cardList: [
        {
          img: require("../assets/images/chat.webp"),
          title: "前期沟通阶段",
          desc: "了解项目情况及客户需求，提供项目建议"
        },
        {
          img: require("../assets/images/plan.webp"),
          title: "提交项目设计计划服务书",
          desc: "包含工作范围、服务内容、时间计划、费用报价"
        },
        {
          img: require("../assets/images/sign.webp"),
          title: "签约阶段",
          desc: "签约完成后，提交概念方案-方案深化设计"
        },
        {
          img: require("../assets/images/drawing.webp"),
          title: "施工图阶段",
          desc: "包含、平面、立面、天花及节点详图、强弱电综合图等"
        },
        {
          img: require("../assets/images/achievement.webp"),
          title: "项目成果文件提交",
          desc: "包含材料、灯光、家具、艺术品陈设设计"
        },
        {
          img: require("../assets/images/track.webp"),
          title: "项目施工现场跟踪服务",
          desc: "解决现场施工过程中图纸变更等问题，直至项目完成交付使用"
        }
      ]
    };
  }
};
</script>
<style lang="less" scoped>
.company {
  width: 100%;
  overflow: hidden;
  box-sizing: border-box;
  margin: 10px 0;
  text-align: center;
  .time {
    font-size: 13px;
    color: #999;
  }

  .card{
    display: inline-block;
    width: 400px;
    margin: 20px;
    .image {
      display: block;
      margin: 0 auto;
    }
  }



  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }

  .clearfix:after {
    clear: both;
  }
}
</style>
