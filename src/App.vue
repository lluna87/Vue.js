<template>
  <h1>VueJS</h1>
  <div>
    <h2>Car - Options</h2>
    <Car3Options />
  </div>
  <hr>
  <div>
    <h2>Car - Composition</h2>
    <Car3Composition />
  </div>
  <hr>
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
import Car3Options from "./components/Car3Options";
import Car3Composition from "./components/Car3Composition";

export default {
    components: {
        Car,
        Car2,
        Car3Options,
        Car3Composition
    }
}
</script>

<style>

</style>