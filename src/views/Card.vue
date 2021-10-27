<template>
  <el-row>
    <el-col
        v-for="(o, index) in 4"
        :key="o"
        :span="4"
        :offset="index > 0 ? 1 : 0"
    >
      <el-card :body-style="{ padding: '10px' }">
        <img
            :src="imgSrc"
            class="image"
        />
        <div style="padding: 14px">
          <span>
            <slot>{{ content }}</slot>
          </span>
        </div>
      </el-card>
    </el-col>
  </el-row>
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue'

export default defineComponent({
  props: {
    content: {
      type: String,
      default: 'content will be injected here automatically '
    },
    imgSrc: {
      type: String,
      default: 'https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png'
    }
  },
  setup(props, context) {
    const currentDate = ref(new Date())
    console.log('--ref--')
    console.log(ref)
    console.log('--context--')
    console.dir(context)
    return {
      currentDate,
    }
  },
})
</script>

<style>
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.button {
  padding: 0;
  min-height: auto;
}

.image {
  width: 100%;
  display: block;
}

.el-row {
  justify-content: center;
  align-items: center;
  /*border:1px solid red ;*/
}
</style>