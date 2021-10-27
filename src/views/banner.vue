<template>
  <section class="nav-bar">
    <div class="brand"><img src="../assets/maxvision-logo.png" alt="">
      <span>AI 开放平台</span>
    </div>
    <ul class="center-nav">
      <li v-for="item in banner" :key="item.id"><span>{{ item }}</span></li>
    </ul>
    <span class="pull-right">console</span>
  </section>

  <section class="carousel-container">
    <div class="block">
      <el-carousel height="600px" interval="3000">
        <el-carousel-item v-for="item in imgSource" :key="item">
          <h3 class="small"><img :src="item" :alt="item"></h3>
        </el-carousel-item>
      </el-carousel>
    </div>
  </section>
</template>
<script>

export default {
  name: "banner",
  data() {
    return {
      banner: ['首页', 'AI能力', '产品中心', '解决方案'],
      imgSource: ['https://i.loli.net/2021/10/27/Q5PnTZcHD8sXl1w.png',
        'https://i.loli.net/2021/10/27/ajvhY3SfTJZWdKG.png',
        'https://i.loli.net/2021/10/27/owfXj5blvNyJiBG.jpg']

    }
  },
}
</script>

<style scoped>
.nav-bar {
  z-index: 999;
  position: fixed;
  top: 0;
  width: 100%;
  /*border: 1px solid red;*/
  display: flex;
  justify-content: space-between;
  flex: 1;
  padding: 15px 5%;
  /*background: black;*/
  border-bottom: 1px solid hsla(0, 0%, 100%, .1);

}

.nav-bar .brand {
  text-align: center;
  /*border: 1px solid gold;*/
  display: flex;
  margin-right: 2%;
}

.nav-bar .brand > span {
  margin-left: 5px;
  padding: 5px 0 0 5px;
  font-size: 18px;
  font-weight: 700;
  line-height: 31px;
  color: #fff;
  border-left: 3px solid white;
}


.nav-bar > .center-nav {
  width: 20%;
  padding: 5px 0 0 5px;
  /*border: 1px solid red;*/
  display: flex;
  justify-content: space-between;
  flex: 1;
  text-align: center;
  font-size: 14px;
  font-weight: 700;
  line-height: 31px;
  color: #fff;
}


.nav-bar > .pull-right {
  /*margin-left: 5px;*/
  padding: 5px 0 0 0;
  /*border: 1px solid gold;*/
  margin: 0 10% 0 20%;
  text-align: center;
  font-size: 18px;
  font-weight: 700;
  line-height: 31px;
  color: #fff;
}

.carousel-container {

}

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>