<template>
  <div class="serve">
    <div class="bgImg">
      <div class="header_wrap">
        <p class="title">
          专业的设计理念、认真的态度、创意的意识、是本团队崇尚奉行的理念
        </p>
        <p class="title">知识、品质、细节、信赖、创造是我们奉行的核心价值观</p>
      </div>
    </div>
    <div>
      <div class="container_header">
      <p class="title">服务领域设计内容</p>
      <p class="subtitle">SERVICE</p>
      </div>
      <ServiceCard></ServiceCard>
    </div>
    <div>
      <div class="container_header">
      <p class="title">服务具体流程</p>
      <p class="subtitle">COMPANY</p>
      </div>
      <companyCard></companyCard>
    </div>

  </div>
</template>

<script>
import ServiceCard from "../components/serviceCard.vue";
import CompanyCard from "../components/companyCard.vue";
export default {
  name: "service",
  components: {
    ServiceCard,
    CompanyCard
  },
  data() {
    return {

    };
  }
};
</script>
<style lang="less" scoped>
.serve {
  .bgImg {
    height: 300px;
    background-image: url("~@/assets/images/bg.png");
    background-size: cover;
    text-align: center;
    color: #fff;
    position: relative;
    .header_wrap {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      p {
        margin-top: 20px;
      }
    }
  }
  .container_header {
    text-align: center;
    margin-top: 20px;
    .title {
      font-size: 26px;
      font-weight: 800;
    }
  }
}
</style>
