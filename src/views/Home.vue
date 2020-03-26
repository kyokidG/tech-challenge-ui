<template>
  <div class="home flex flex-column justify-between">
    <img alt="Vue logo" src="../assets/logo.png" class="logo" />
    <ProjectInfo title="Tech Challenge for UI Developer position" />
    <h4 class="footer pb-1">
      A project by
      <a href="https://georgebrata.ro">Brata George</a>
    </h4>
  </div>
</template>

<script>
import ProjectInfo from "@/components/ProjectInfo.vue";

export default {
  name: "Home",
  components: {
    ProjectInfo
  }
};
</script>
<style scoped>
.home {
  text-align: center;
  padding: 0 20px;
  height: 100vh;
}
.logo {
  margin: 10px auto;
  width: 15%;
}

</style>