<template>
  <label class="container">
    {{this.label}}
    <input type="radio" :name="id" />
    <span class="checkmark"></span>
  </label>
  <!-- 
  <div class="flex flex-row w-100 mx-1">
    <input type="radio" :id="id" :name="id" />
    <label :for="id">{{this.label}}</label>
  </div>-->
</template>

<script>
export default {
  name: "GRadio",
  props: {
    label: String,
    id: String
  }
};
</script>

<style scoped>
label {
  text-transform: uppercase;
  font-size: 0.6rem;
  padding-top: 0.2rem;
}
/* The container */
.container {
  display: block;
  position: relative;
  padding-left: 35px;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default radio button */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
}

/* Create a custom radio button */
.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 1rem;
  width: 1rem;
  background-color: rgb(0, 0, 0, 0.5);
  border-radius: 100%;
  border: 1px solid var(--primary-color);
}
input:focus + .checkmark {
  box-shadow: 0px 0px 5px 1px var(--primary-color-focus);
}

/* When the radio button is checked, add a blue background */
.container input:checked ~ .checkmark {
  background-color: transparent;
}

/* Create the indicator (the dot/circle - hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the indicator (dot/circle) when checked */
.container input:checked ~ .checkmark:after {
  display: block;
}

/* Style the indicator (dot/circle) */
.container .checkmark:after {
  top: 0.25rem;
  left: 0.25rem;
  width: 0.4rem;
  height: 0.4rem;
  border-radius: 50%;
  background: white;
}
</style>
