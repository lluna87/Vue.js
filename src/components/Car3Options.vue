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
            this.power = this.power + ( (typeof newPower != 'undefined') ? newPower : 1 );
        },
        downPower(newPower) {
            let changeValue =  (typeof newPower != 'undefined') ? newPower : 1;
            this.power = this.power - changeValue < 0 ? 0 : this.power - changeValue;
        }
    }
}
</script>

<style>

</style>