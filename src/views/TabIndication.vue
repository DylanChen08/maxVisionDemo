<template>
  <section class="tab-indication-container">

    <el-tabs v-model="activeName" @tab-click="handleClick">

      <el-tab-pane label="发展趋势" name="first">
        <h1 style="font-size: 30px;font-weight: bold;margin: 30px 0;">发展趋势</h1>
        <card :img-src="src1">
          <span class="card-title">AI推动城市治理，向智慧化转型解决方案</span> <br/>
          <span class="card-content">将先进的深度学习算法引入到人脸检测、比对以及指纹识别等功
          能模块中，使得单个识别模块的可信度显著提高</span>
        </card>
      </el-tab-pane>
      <!-- ******************************************************************-->
      <el-tab-pane label="方案概述" name="second">
        <h1 style="font-size: 30px;font-weight: bold;margin: 30px 0;">方案概述</h1>
        <card :img-src="src2">
          <span class="card-title">AI推动城市治理，向智慧化转型解决方案</span> <br/>
          <span class="card-content">将先进的深度学习算法
            引入到人脸检测、比对以及指纹识别等功
          能模块中，使得单个识别模块的可信度显著提高</span>
        </card>
      </el-tab-pane>
      <!-- ******************************************************************-->
      <el-tab-pane label="核心优势" name="third">
        <h1 style="font-size: 30px;font-weight: bold;margin: 30px 0;">核心优势</h1>
        <card :img-src="src3">
          <span class="card-title">AI推动城市治理，向智慧化转型解决方案</span> <br/>
          <span class="card-content">将先进的深度学习算法引入到人脸检测、比对以及指纹识别等功
          能模块中，使得单个识别模块的可信度显著提高</span>
        </card>
      </el-tab-pane>
      <!-- ******************************************************************-->
      <el-tab-pane label="相关产品" name="fifth">
        <h1 style="font-size: 30px;font-weight: bold;margin: 30px 0;">相关产品</h1>
        <card :img-src="src4">
          <span class="card-title">AI推动城市治理，向智慧化转型解决方案</span> <br/>
          <span class="card-content">将先进的深度学习算法引入到人脸检测、比对以及指纹识别等功
          能模块中，使得单个识别模块的可信度显著提高</span>
        </card>
      </el-tab-pane>
      <!-- ******************************************************************-->
      <el-tab-pane label="应用场景" name="sixth">
        <h1 style="font-size: 30px;font-weight: bold;margin: 30px 0;">应用场景</h1>
        <card :img-src="src5">
          <span class="card-title">AI推动城市治理，向智慧化转型解决方案</span> <br/>
          <span class="card-content">将先进的深度学习算法引入到人脸检测、比对以及指纹识别等功
          能模块中，使得单个识别模块的可信度显著提高</span>
        </card>
      </el-tab-pane>
      <!-- ******************************************************************-->
      <el-tab-pane label="相关解决方案" name="seventh">
        <h1 style="font-size: 30px;font-weight: bold;margin: 30px 0;">相关解决方案</h1>
        <card :img-src="src6">
          <span class="card-title">AI推动城市治理，向智慧化转型解决方案</span> <br/>
          <span class="card-content">将先进的深度学习算法引入到人脸检测、比对以及指纹识别等功
          能模块中，使得单个识别模块的可信度显著提高</span>
        </card>
      </el-tab-pane>
    </el-tabs>

  </section>

</template>
<script lang="ts">
import card from "@/views/Card.vue";

export default {
  data() {
    return {
      activeName: 'first',
      src1: 'https://i.loli.net/2021/10/27/Q5PnTZcHD8sXl1w.png',
      src2: 'https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png',
      src3: 'https://i.loli.net/2021/10/27/ajvhY3SfTJZWdKG.png',
      src4: 'https://i.loli.net/2021/10/27/owfXj5blvNyJiBG.jpg',
      src5: 'https://i.loli.net/2021/10/27/vhGjdT3mPeUfFcg.png',
      src6: 'https://i.loli.net/2021/10/27/4PCRi1kSWoZGc7T.png'
    }
  },
  components: {
    card
  },
  methods: {
    handleClick(tab: any, event: any) {
      console.log(tab, event)
    },
  },
}
</script>

<style>
.tab-indication-container {
  margin-top: 50px;
}

.card-title {
  /*border: 1px solid red;*/
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12px;
  white-space: nowrap;
}

.card-content {
  text-align: left;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>