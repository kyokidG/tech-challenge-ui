<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" style="margin: 0 auto;">
    <ProjectInfo title="Welcome to George Brata's Implementation of UI Tech Challenge"/>
  </div>
</template>

<script>
import ProjectInfo from '@/components/ProjectInfo.vue'

export default {
  name: 'Home',
  components: {
    ProjectInfo
  }
}
</script>
<style scoped>
.home {
  text-align: center;
}
</style>