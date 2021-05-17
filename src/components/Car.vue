<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Color: {{ color[1] }}</p>
  <p>Precio: {{ precio }} U$D</p>
  <p>Potencia: {{ power }} CV</p>
  <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
</template>

<script>
export default {
    // data() {
    //     return {
    //         brand: "Audi",
    //         model: 'A4',
    //         color: ["Azul", "Rojo", "Verde"],
    //         price: 10000,
    //         power: 180,
    //         mensaje: {
    //             title: "Hola Mundo",
    //             text: "Adiós",
    //         }
    //     }
    // }
    setup() {
        const brand = "Audi";
        const model = "A4";
        const color = ["Azul", "Rojo", "Verde"];
        const price = 10000;
        const power = 180;

        const mensaje = {
                title: "Hola Mundo",
                text: "Adiós"
            };

        return {
            brand,
            model,
            color,
            price,
            power,
            mensaje
        }
    }

}
</script>

<style>

</style>