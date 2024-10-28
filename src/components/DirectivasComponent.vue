<template>
  <div>
    <h1>Ejemplo Directivas VUE</h1>
    <!-- EL SIMBOLO DOLAR NOS PERMITE ACCEDER A ELEMENTOS -->
    {{ $data }}
    <br />
    <br />
    <label>Introduzca un número</label>
    <input type="number" v-model="numero" />
    <h3 v-if="numero > 0" style="color: green">POSITIVO</h3>
    <h3 v-else-if="numero < 0" style="color: red">NEGATIVO</h3>
    <h3 v-else style="color: blue">CERO</h3>
    <ul v-if="series.length > 0">
      <li v-for="serie in series" :key="serie">
        {{ serie }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "DirectivasComponent",
  
  data() {
    return {
      series: [
        "Juego de tronos",
        "Futurama",
        "Stranger Things",
        "Mr. Robot",
        "The Boys",
      ],
      numero: 0,
      nombre: "Manuel",
      edad: 28,
    };
  },
};
</script>
