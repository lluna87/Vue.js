<template>
  <h3>Coche</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Color: 
      <!-- <span v-for="(color, index) in colors" :key="index">
          {{ index + 1 }}: {{ color }} -
      </span> -->
  </p>
  <ul>
      <li v-for="(color, index) in colors" :key="index">{{ index + 1 }}: {{ color }}</li>
  </ul>
  <p>Precio: {{ precio }} U$D</p>
  <p>Potencia: {{ power }} CV</p>
  <p>{{ mensaje.title }} - {{ mensaje.text }}</p>
</template>

<script>
export default {
    setup() {
        const brand = "Audi";
        const model = "A4";
        const colors = ["Azul", "Rojo", "Verde", "Amarillo"];
        const price = 10000;
        const power = 180;

        const mensaje = {
                title: "Hola Mundo",
                text: "Adiós"
            };

        return {
            brand,
            model,
            colors,
            price,
            power,
            mensaje
        }
    }
    // Alternativa 1
    // data() {
    //     return {
    //         brand: "Audi",
    //         model: 'A4',
    //         colors: ["Azul", "Rojo", "Verde"],
    //         price: 10000,
    //         power: 180,
    //         mensaje: {
    //             title: "Hola Mundo",
    //             text: "Adiós",
    //         }
    //     }
    // }
}
</script>

<style>

</style>