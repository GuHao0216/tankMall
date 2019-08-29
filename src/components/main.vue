<template>
  <div class="main">
    <el-container>
      <el-header>
        <Header></Header>
      </el-header>
      <el-main>
        <el-carousel trigger="click" class="banner" :height="imgHeight+'px'">
          <el-carousel-item v-for="item in imagesbox" :key="item.id">
            <img ref="image" :src="item.src" class="bannerimg" />
          </el-carousel-item>
        </el-carousel>
        <el-row style="height:200px;margin: 25px 0">
          <el-col :span="6">
            <el-card class="cardSmall" :body-style="{ padding:0,height:'100%' }" shadow="hover">
              <img
                src="https://resource.smartisan.com/resource/6/610400xinpinpeijian.jpg"
                class="cardImg"
                alt
              />
            </el-card>
          </el-col>
          <el-col :span="6">
            <el-card class="cardSmall" :body-style="{ padding:0,height:'100%' }" shadow="hover">
              <img
                src="https://resource.smartisan.com/resource/4/489673079577637073.png"
                class="cardImg"
                alt
              />
            </el-card>
          </el-col>
          <el-col :span="6">
            <el-card class="cardSmall" :body-style="{ padding:0,height:'100%' }" shadow="hover">
              <img
                src="https://resource.smartisan.com/resource/6/610400xinpinpeijian.jpg"
                class="cardImg"
                alt
              />
            </el-card>
          </el-col>
          <el-col :span="6">
            <el-card class="cardSmall" :body-style="{padding:0, height:'100%' }" shadow="hover">
              <img
                src="https://resource.smartisan.com/resource/4/489673079577637073.png"
                class="cardImg"
                alt
              />
            </el-card>
          </el-col>
        </el-row>

        <el-row style="height:492px;margin: 25px 0">
          <div class="title">111</div>
          <el-row class="bigImg">
            <el-col :span="12">
              <el-card class="cardSmall" :body-style="{padding:0, height:'100%' }" shadow="hover">
                <img
                  src="https://resource.smartisan.com/resource/804edf579887b3e1fae4e20a379be5b5.png"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
            <el-col :span="12">
              <el-card class="cardSmall" :body-style="{padding:0, height:'100%' }" shadow="hover">
                <img
                  src="https://resource.smartisan.com/resource/804edf579887b3e1fae4e20a379be5b5.png"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
          </el-row>
        </el-row>

        <el-row style="height:922px;margin: 25px 0">
          <div class="title">111</div>
          <el-row class="middle">
            <el-col :span="12">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
            <el-col :span="6">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
            <el-col :span="6">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
          </el-row>
          <el-row class="middle">
            <el-col :span="6">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
            <el-col :span="6">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
            <el-col :span="6">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
            <el-col :span="6">
              <el-card class="cardSmall" shadow="hover" :body-style="{padding:0, height:'100%' }">
                <img
                  src="https://resource.smartisan.com/resource/1/1220858shoujilouceng.jpg"
                  alt
                  class="cardImg"
                />
              </el-card>
            </el-col>
          </el-row>
        </el-row>
      </el-main>
      <el-footer>Footer</el-footer>
    </el-container>
    <el-backtop target="main"></el-backtop>
  </div>
</template>

<script>
import Header from "./template/header.vue";
export default {
  name: "Main",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      input1: "",
      imagesbox: [
        { id: 0, src: require("../assets/banner/banner1.png") },
        { id: 1, src: require("../assets/banner/banner2.png") },
        { id: 2, src: require("../assets/banner/banner3.png") },
        { id: 3, src: require("../assets/banner/banner4.png") }
      ],
      imgHeight: ""
    };
  },
  components: {
    Header
  },
  methods: {
    imgLoad() {
      this.$nextTick(function() {
        // 获取窗口宽度*图片的比例，定义页面初始的轮播图高度
        this.imgHeight = this.$refs.image[0].height;
        console.log(this.imgHeight);
      });
    }
  },
  mounted() {
    this.imgLoad();
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {
  margin: 0 !important;
}
.title {
  padding-left: 30px;
  position: relative;
  z-index: 10;
  height: 60px;
  padding: 0 10px 0 24px;
  border-bottom: 1px solid #d4d4d4;
  border-radius: 8px 8px 0 0;
  box-shadow: 0 1px 7px rgba(0, 0, 0, 0.06);
  background: #f3f3f3;
  background: linear-gradient(#fbfbfb, #ececec);
  line-height: 60px;
  font-size: 18px;
  color: #333;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -ms-flex-align: center;
  align-items: center;
}
.bigImg{
  height: calc(100% - 60px)!important;
}
.cardSmall {
  height: 100%;
  display: block;
}
.cardImg {
  width: 100%;
  height: 100%;
}
.middle{
  height: calc(50% - 30px)!important;
}
.banner {
  width: 100%;
}
.bannerimg {
  width: 100%;
}

.el-header {
  height: 100px !important;
  width: 100%;
  border-bottom: 1px solid #cccccc;

  /* position: fixed; */
  /* z-index:auto; */
  background-color: white;
}
.el-row {
  height: 100%;
}
.el-col {
  height: 100%;
}
.el-main {
  width: 80%;
  margin: 10px 149.6px;
}
/* .el-footer{
    position: relative;
    margin-bottom: 20px;
    height: 350px;
} */
</style>