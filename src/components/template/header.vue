<template>
  <div class="header">
    <el-row style="  position:relative;margin: 0 149.600px;">
      <el-col :span="18">
        <img src="../../assets/tank.png" alt class="logo" />
        <el-input placeholder="请输入商品信息" v-model="input1" class="search">
          <el-button slot="append" icon="el-icon-search"></el-button>
        </el-input>
      </el-col>
      <el-col :span="6">
        <el-row>
          <el-button
            type="plain"
            icon="el-icon-user"
            style="margin-top: 32px;border:none;  margin-left:41px"
          ></el-button>

          <el-divider direction="vertical"></el-divider>

          <el-button
            type="plain"
            icon="el-icon-shopping-cart-2"
            style="margin-top: 32px;border:none;"
          ></el-button>
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "header",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      input1:''
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  height: 100px !important;
  width: 100%;
  border-bottom: 1px solid #cccccc;

  /* position: fixed; */
  /* z-index:auto; */
  background-color: white;
}
.logo {
  float: left;
  margin-top: 10px;
  width: auto;
  height: auto;
  max-width: 70%;
  max-height: 70%;
}
.search {
  float: right;
  margin-top: 30px;
  width: auto;
  height: auto;
}
.el-row {
  height: 100%;
}
.el-col {
  height: 100%;
}
</style>