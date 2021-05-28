<template>
  <h3>Coche - Options</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower()">Aumentar</button>
  <button @click="upPower(1000)">Aumentar (1000)</button>
  <button @click="downPower()">Disminuir</button>
  <button @click="downPower(500)">Disminuir (500)</button>
</template>

<script>
import { ref } from 'vue';

export default {
    setup() {
        const brand = "Seat";
        const model = "Leon";
        let power = ref(50);

        const upPower = (newPower) => {
            power.value = power.value + ( (typeof newPower != 'undefined') ? newPower : 1 );
        };
        const downPower = (newPower) => {
            let changeValue =  (typeof newPower != 'undefined') ? newPower : 1;
            power.value = power.value - changeValue < 0 ? 0 : power.value - changeValue;
        }

        return {
            brand,
            model,
            power,
            upPower,
            downPower
        }
    }
}
</script>

<style>

</style>