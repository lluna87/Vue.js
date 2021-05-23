<template>
  <h1>VueJS</h1>
  <div>
    <h2>Car 2</h2>
    <Car2 />
  </div>
  <hr>
  <div>
    <h2>Car</h2>
    <Car></Car>
  </div>
  
</template>

<script>

import Car from "./components/Car";
import Car2 from "./components/Car2";

export default {
    components: {
        Car,
        Car2
    }
}
</script>

<style>

</style>