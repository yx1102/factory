<template>
  <div class="contact">
    <div class="bgImg"></div>
    <div class="container_header">
      <p class="title">联系</p>
      <p class="subtitle">CONTACT</p>
    </div>
    <!-- <div class="container_content">
      <div class="contactinfo">
        <h3 class="contact_name">
          网站建设文化传播有限公司
        </h3>
        <p class="contact_add">
          地址：中国地区XX分区5A写字楼8-88室
        </p>
        <p class="contact_zip">邮编：100000</p>
        <p class="contact_tel">电话：XXX</p>
        <p class="contact_mob">手机：XXX</p>
        <p class="contact_fax">传真：XXX</p>
        <p class="contact_eml">邮箱：XXX</p>
      </div>
    </div> -->
    <div class="container_form">
      <el-form
        :model="ruleForm"
        :rules="rules"
        ref="ruleForm"
        label-width="100px"
      >
        <el-form-item label="姓名" prop="name">
          <el-input v-model="ruleForm.name"></el-input>
        </el-form-item>
        <el-form-item label="电话" prop="tel">
          <el-input v-model="ruleForm.tel"></el-input>
        </el-form-item>
        <el-form-item label="内容" prop="desc">
          <el-input
            type="textarea"
            :rows="4"
            v-model="ruleForm.desc"
          ></el-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary">提交</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      ruleForm: {
        name: "",
        tel: "",
        desc: ""
      },
      rules: {
        name: [
          { required: true, message: "请输入名称", trigger: "blur" },
          { min: 3, max: 5, message: "长度在 3 到 5 个字符", trigger: "blur" }
        ],
        tel: [{ required: true, message: "请输入电话", trigger: "blur" }]
      }
    };
  }
};
</script>
<style lang="less" scoped>
.contact {
  width: 100%;
  height: 100%;
  .bgImg {
    background-image: url("~@/assets/images/contact.jpg");
    height: 300px;
    background-size: cover;
  }
  .container_header {
    text-align: center;
    margin-top: 20px;
    .title {
      font-size: 26px;
      font-weight: 800;
    }
  }
  .container_content {
    margin: 20px 340px;
  }
  .subtitle,
  .contact_zip,
  .contact_tel,
  .contact_mob,
  .contact_fax,
  .contact_add,
  .contact_eml {
    color: #333;
  }

  .container_form{
    margin: 0 280px;
  }
}
</style>
