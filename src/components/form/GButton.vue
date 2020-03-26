<template>
  <button type="button">{{this.label}}</button>
</template>

<script>
export default {
  name: "GButton",
  props: {
    label: String
  }
};
</script>

<style scoped>
button {
    padding: 10px 20px;
    font-size: 1.1rem;
    text-transform: uppercase;
    color: white;
    background-color: rgb(265,265,265, 0.2);
    width: 100%;
    cursor: pointer;
    border: 3px solid transparent;
    outline: none;
}
button:hover, button:focus {
    border: 3px solid white;
    background-color: transparent;
}
</style>
