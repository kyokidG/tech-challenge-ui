<template>
  <div class="input-container flex flex-column w-100">
    <label :for="id" class="g-form-label">{{this.label}}</label>
    <input
      :type="type"
      :id="id"
      :name="id"
      class="g-form-element"
      :class="{'invalid': hasErrors, 'valid': isValid}"
      v-model="value"
    />
    <img src="@/assets/white-checkmark.png" height="15px" width="15px" class="icon-valid">
  </div>
</template>

<script>
export default {
  name: "GInput",
  props: {
    label: String,
    id: String,
    type: {
      type: String,
      default: "text"
    }
  },
  watch: {
      value: function(newVal) {
          this.isValid = newVal !== ''
          this.hasErrors = !this.isValid
      }
  },
  data() {
    return {
      isValid: false,
      hasErrors: false,
      value: ''
    };
  },
  mounted() {
      //according to specs, the Address field should initialize with an error
      if(this.label === 'Address') {
          this.hasErrors = true
      }
  }
};
</script>

<style scoped>
input:focus {
  border: 1px solid var(--primary-color-focus);
  outline: none;
}
input.invalid {
  border: 1px solid var(--primary-danger);
}
.input-container {
    position: relative;
}
input + .icon-valid {
    display: none;
}
input.valid + .icon-valid {
    display: block;
    position: absolute;
    right: 1rem;
    top: 1.9rem;
}
</style>
