<template>
  <div class="register-page">
    <div class="register-modal-container flex flex-column justify-between">
      <div class="modal-header text-center">
        <h1>Register</h1>
        <p class="info-text">Please finalise your registration before you can proceed</p>
      </div>
      <div class="modal-body flex justify-between">
        <div class="column mx-1">
          <div class="row multiple w-100">
            <g-input label="First name" id="fname" class="mr-1"></g-input>
            <g-input label="Last name" id="lname"></g-input>
          </div>
          <div class="row w-100">
            <g-input class="flex-grow-2 mr-1" label="Date of birth" id="birth" type="date"></g-input>
            <div class="flex-grow-1 flex flex-column justify-around pt-1">
              <g-radio label="Male" id="gender"></g-radio>
              <g-radio label="female" id="gender"></g-radio>
            </div>
          </div>
          <div class="row w-100">
            <g-input label="Address" id="address" class="w-100"></g-input>
          </div>
        </div>
        <div class="column mx-1">
          <div class="row multiple w-100">
            <g-input label="Postcode" id="postcode" class="mr-1"></g-input>
            <g-input label="City" id="city"></g-input>
          </div>
          <div class="row w-100">
            <g-select label="Country" id="country" class="w-100" :options="countries"></g-select>
          </div>
          <div class="row w-100">
            <g-select
              label="Country code"
              id="country-code"
              :options="countryCodes"
              class="w-100 mr-1"
            ></g-select>
            <g-input label="Phone number" id="phone"></g-input>
          </div>
        </div>
      </div>
      <div class="modal-footer text-center m-1">
        <g-button label="Complete registration"></g-button>
        <p class="info-text">you will then confirm your deposit</p>
      </div>
    </div>
  </div>
</template>
<script>
import GButton from "@/components/form/GButton.vue";
import GInput from "@/components/form/GInput.vue";
import GRadio from "@/components/form/GRadio.vue";
import GSelect from "@/components/form/GSelect.vue";

export default {
  name: "Home",
  components: {
    GButton,
    GInput,
    GRadio,
    GSelect
  },
  data() {
    return {
      countries: ["Romania", "Germany", "Italy"],
      countryCodes: ["+40", "+00", "030"]
    };
  }
};
</script>
<style scoped>
/* GENERAL CSS */
.register-page {
  min-height: 100vh;
  background-image: url("../assets/background.jpg");
  background-repeat: no-repeat;
  background-position-x: 50%;
  background-position-y: 50%;
  background-size: auto 100%;
  background-color: black;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-content: center;
}
.register-modal-container {
  height: auto;
  width: auto;
  border: 0;
  max-width: 100%;
}
.modal-header {
  text-transform: uppercase;
}
.modal-body {
  flex-direction: column;
}
.row {
  display: flex;
  justify-content: space-around;
  margin: 1rem 0;
}
.row.multiple div {
  max-width: calc(50% - .5rem);
}
.info-text {
  text-transform: uppercase;
  font-size: 0.8rem;
}

/* MOBILE CSS */
@media (min-width: 576px) {
  .register-page {
    min-height: 100vh;
  }
  .modal-header h1 {
    margin-top: 20px;
  }
  .row.multiple div {
    max-width: 50%;
  }
}

/* TABLET CSS */
@media (min-width: 768px) {
  .register-modal-container {
    padding: 10px;
  }
  .modal-body {
    flex-direction: row;
  }
  .register-modal-container {
    padding: 30px;
    border: 1px solid var(--primary-color);
    box-shadow: 0px 0px 5px 1px var(--primary-color);
    border-radius: 2px;
  }
}

/* DESKTOP */
@media (min-width: 1367px) {
  @import url("https://fonts.googleapis.com/css?family=Alfa+Slab+One&display=swap");

  .modal-header h1 {
    font-family: "Alfa Slab One";
    font-size: 3rem;
    margin-top: 0;
  }
}

@media (min-width: 1200px) {
}
</style>