<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <p>
      Check out the <router-link to="/register">Register Page</router-link> to preview the implementation. <br>
    </p>
    <h3>Approach</h3>
    <p>Project was scaffolded using vue-cli using minimal setup configuration. <br>It only has 2 routes and each page is lazy-loaded on enter, to reduce intial budle size and improve performance.</p>
    <p>The <router-link to="/register">/register</router-link> page is built with mobile-first capabilities, but it supports responsive layout with 3 breakpoints for mobile, tablet and large desktop.</p><br><br>
    <h3>Libraries & Tools used</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">VueJS</a></li>
      <li><a href="https://cli.vuejs.org/" target="_blank" rel="noopener">vue-cli</a></li>
      <li><a href="https://router.vuejs.org/" target="_blank" rel="noopener">vue-router</a></li>
    </ul>
    <ul>
      <li><a href="https://babeljs.io/" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://eslint.org/" target="_blank" rel="noopener">eslint</a></li>
      <li><a href="https://github.com/" target="_blank" rel="noopener">GitHub</a></li>
      <li><a href="https://www.netlify.com/" target="_blank" rel="noopener">Netlify</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ProjectInfo',
  props: {
    title: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
</style>
