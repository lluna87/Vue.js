<template>
  <h3>Coche - Options</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(1000)">Aumentar</button>
  <button @click="downPower(500)">Disminuir</button>
</template>

<script>
export default {
    data() {
        const brand = "Seat";
        const model = "Leon";
        const power = 50;

        return {
            brand: brand,
            model: model,
            power: power
        }
    },
    methods: {
        upPower(newPower) {
            console.log("Aumentando potencia: " + newPower);
        },
        downPower(newPower) {
            console.log("Disminuyendo potencia: " + newPower);
        } ,
    }
}
</script>

<style>

</style>