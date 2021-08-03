<template>
  <div class="wrap">
    <h3>小强技术研究专区</h3>
    <p>用于沉淀记录技术相关，包括前端、后端、服务器相关知识</p>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'Home',
  setup () {
    const link = ref('https://beian.miit.gov.cn/#/Integrated/index')

    return { link }
  }
})
</script>
<style lang="scss" scoped>

</style>
