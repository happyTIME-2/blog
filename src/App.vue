<template>
  <el-container>
    <el-header>
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item el-menu-item index="1">
          <router-link to="/">主页</router-link>
        </el-menu-item>
        <el-menu-item index="2"><router-link to="/about">About Me</router-link></el-menu-item>
      </el-menu>
    </el-header>
    <el-main>
      <router-view />
    </el-main>
    <el-footer>
      <el-link :href="link" target="_blank" :underline="false">粤ICP备18074936号</el-link>
    </el-footer>
  </el-container>
</template>
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup () {
    const activeIndex = ref('1')

    const handleSelect = (key, keyPath) => {
      console.log(key, keyPath)
    }

    const link = ref('https://beian.miit.gov.cn/')

    return {
      activeIndex,
      link,
      handleSelect
    }
  }
})
</script>
<style lang="scss">
.el-header, .el-footer {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #D3DCE6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
