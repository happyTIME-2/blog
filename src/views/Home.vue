<template>
  <div class="home">
    <home-com />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import HomeCom from '@/components/Home.vue'
@Options({
  components: {
    HomeCom
  }
})
export default class Home extends Vue {}
</script>
