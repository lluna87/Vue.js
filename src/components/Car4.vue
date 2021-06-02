<template>
  <h3>Coche - Options</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPowerFn">Disminuir</button>
</template>

<script>
export default {
    props: {
        // power: String
        power: {
            type: Number,
            default: 60
        },
        upPower: Function,
        downPower: Function
    },
    emits: ["downPower"],
    setup(props,context) { /*setup(props) {*/
        const brand = "Audi";
        const model = "A4";

        const downPowerFn = () => {
            context.emit("downPower");
        }

        return {
            brand,
            model,
            downPowerFn
        }
    }
}
</script>

<style>

</style>