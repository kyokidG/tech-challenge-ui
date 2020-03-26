<template>
  <div class="flex flex-column">
    <label :for="id" class="g-form-label">{{this.label}}</label>
    <select :id="id" :name="id" class="select-css g-form-element">
      <option v-for="option in options" :key="option" :value="option">{{option}}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "GSelect",
  props: {
    label: String,
    id: String,
    options: Array
  }
};
</script>

<style scoped>
.select-css {
  display: block;
  color: white;
  box-sizing: border-box;
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none;
  background-image: url("https://i.ya-webdesign.com/images/white-arrow-down-png.png");
  background-repeat: no-repeat, repeat;
  background-position: right 0.7em top 50%, 0 0;
  background-size: 1rem auto, 100%;
  outline: none;
}
.select-css::-ms-expand {
  display: none;
}
.select-css:focus {
    box-shadow: 0px 0px 5px .5px var(--primary-color-focus);
}
.select-css option {
  font-weight: normal;
}
</style>