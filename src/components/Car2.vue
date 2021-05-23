<template>
  <h3>Coche - Prueba condicionales</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Urban Powers: Power &lt; 300 cv</p>
  <p>Power: {{ powers }}</p>
  <h4>IF</h4>
  <div class="flex-row">
    <div class="flex-column">
      <p>
        <b>Opcion 1:</b> Error, dibuja todos los bullets, porque el condicional
        no esta en el li, sino en el contenido de dicho li.
        <br />
        Itera por cada item de la coleccion, siempre agrega un li, solo agrega
        el texto de los que cumplen la condicion
      </p>
      <ul>
        <li v-for="(power, index) in powers" :key="index">
          <template v-if="power < 300">{{ power }}</template>
        </li>
      </ul>
    </div>
    <div class="flex-column">
      <p>
        <b>Opcion 2:</b> Correcto, dibuja solo los bullets que hacen falta.
        <br />
        Itera por cada item de la coleccion y solo agrega un "li" si el valor
        cumple la condicion
      </p>
      <ul>
        <template v-for="(power, index) in powers" :key="index">
          <li v-if="power < 300">{{ power }}</li>
        </template>
      </ul>
    </div>
  </div>
  <h4>IF-ELSE</h4>
  <p>Mostrar valores &lt; 200 y valores &gt;&equals; 500</p>
  <ul>
    <template v-for="(power, index) in powers" :key="index">
      <li v-if="power < 200">{{ power }}</li>
      <li v-else class="red-bold">* {{ power }} *</li>
    </template>
  </ul>
  <h4>IF-ELSE-IF</h4>
  <p>Mostrar valores &lt; 200 y valores &gt;&equals; 500</p>
  <ul>
    <template v-for="(power, index) in powers" :key="index">
      <li v-if="power < 100" class="green-bold">{{ power }}</li>
      <li v-else-if="power >= 500" class="red-bold">{{ power }}</li>
      <li v-else-if="power >= 200 && power < 310" class="blue-bold">
        {{ power }}
      </li>
      <li v-else class="grey-bold">{{ power }}</li>
    </template>
  </ul>
</template>

<script>
export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500];

    return {
      brand,
      model,
      powers,
    };
  },
};
</script>

<style>
p {
  margin-block-start: 0.4em;
  margin-block-end: 0em;
}
h1,
h2,
h3,
h4 {
  display: block;
  margin-block-start: 0.4em;
  margin-block-end: 0em;
}
.flex-row {
  display: flex;
  flex-direction: row;
}
.flex-column {
  display: flex;
  flex-direction: column;
  margin-right: 10px;
}
.red-bold {
  color: darkred;
  font-style: italic;
  font-weight: bold;
}
.green-bold {
  color: darkgreen;
  font-style: italic;
  font-weight: bold;
}
.blue-bold {
  color: darkblue;
  font-style: italic;
  font-weight: bold;
}
.grey-bold {
  color: darkgrey;
  font-style: italic;
  font-weight: bold;
}
</style>