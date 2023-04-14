<template>
  <div class="container">
    <div class="country-container">
      <h2>Select a Country to View</h2>
      <ul class="country" v-for="country in countryDisplay" :key="country.id">
        <li>{{ country.country }}</li>
      </ul>
    </div>
    <div class="container-details">
      <h2>You have selected</h2>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      countries: [],
    };
  },

  mounted() {
    axios
      .get(
        "https://countriesnow.space/api/v0.1/countries"
        // "https://countriesnow.space/api/v0.1/countries/flag/images"
      )
      .then((response) => {
        this.countries = response.data.data;
        console.log(response.data.data);
      })
      .catch((error) => {
        console.log(error);
      });
  },
  computed: {
    countryDisplay() {
      return this.countries;
    },
  },
};
</script>

<style scoped>
.container {
  position: relative;
  left: 0;
  top: 100px;
  /* border: 1px solid red; */
  /* background-color: aquamarine; */
  width: 100%;
  height: 100%;
  border-radius: 10px;
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 1rem;
  flex-wrap: nowrap;
}
.country-container {
  background-color: aliceblue;
  border: 2px solid black;
  border-radius: 10px;
  height: 100%;
}
.container-details {
  background-color: aliceblue;
  border: 2px solid black;
  border-radius: 10px;
  height: 100%;
}
</style>
