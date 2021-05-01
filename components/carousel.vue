<template>
  <div>
     <el-carousel height="500px">
      <el-carousel-item v-for="item in imgList" :key="item.img">
        <img :src="item.img" alt="" class="img">
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  name:'',
  data () {
    return {
      imgList: [
        {
          img: require("../assets/images/10.jpg"),
        },
        {
          img: require("../assets/images/11.jpg"),
        },
        {
          img: require("../assets/images/12.jpg"),
        },
      ]
    };
  },
}

</script>
<style lang='less' scoped>
.img{
  width: 100%;
}
</style>
