<template>
  <h1>VueJS</h1>
  <div>
    <h2>Car 4: Props</h2>
    <!-- <Car4 power="power" /> --> <!-- TEXTO -->
    <Car4 :power="power" :upPower="upPower" @downPower="downPower" />
  </div>
  <hr>
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
import Car4 from "./components/Car4";
import { ref } from 'vue';

export default {
    components: {
        Car,
        Car2,
        Car3Options,
        Car3Composition,
        Car4
    },
    setup() {
      let power = ref(73);

      const upPower = ()  =>  { power.value++; }
      const downPower = ()  =>  { power.value--; }

      return { power, upPower, downPower };
    }
}
</script>

<style>

</style>