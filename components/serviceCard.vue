<template>
  <div class="card">
    <el-card
      shadow="hover"
      class="box-card"
      v-for="item in cardData"
      :key="item.title"
    >
      <div slot="header" class="cardTitle">
        <span>{{ item.title }}</span>
      </div>
      <div v-for="o in item.desc" :key="o" class="text item">
        {{ o }}
      </div>
    </el-card>
  </div>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      cardData: [
        {
          title: "室内空间规划内容",
          desc: [
            "业态组合（商业)",
            "室内空间动线规划",
            "室内空间功能规划",
            "室内概念设计",
            "室内方案设计",
            "物料应用设计",
            "样板间设计（酒店）",
            "施工图深化设计"
          ]
        },
        {
          title: "软装、陈设设计内容",
          desc: [
            "软装陈设搭配设计",
            "艺术灯饰设计",
            "布艺灯饰设计",
            "家具设计",
            "艺术品收集",
            "艺术品搭配设计"
          ]
        },
        {
          title: "灯光、机电规划内容",
          desc: [
            "项目配套设施规划",
            "安防设计",
            "水、电、暖通设计",
            "智能化设计",
            "室内灯光亮化设计"
          ]
        }
      ]
    };
  }
};
</script>
<style lang="less" scoped>
.card {
  width: 100%;
  overflow-x: hidden;
  box-sizing: border-box;
  display: flex;
  justify-content: center;
  .box-card {
    width: 300px;
    height: 350px;
    margin-top: 50px;
    margin-left: 40px;
    display: inline-block;
    .cardTitle{
      font-weight: 700;
      font-size: 20px;
      text-align: center;
    }
    .text{
      line-height: 30px;
    }
  }
}
</style>
