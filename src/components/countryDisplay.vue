<template>
  <div class="container">
    <div class="country-container">
      <h2>Select a Country to View</h2>







    </div>
    <div class="container-details">
       <h2>You have selected    </h2> 
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container{
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

}
.country-container{
 
    background-color: aliceblue;
    border: 2px solid black;
    border-radius: 10px;
    height: 100%;
}
.container-details{
    background-color: aliceblue;
    border: 2px solid black;
    border-radius: 10px;
    height: 100%;
}
</style>
