<template>
  <h1>Números Par o Impar</h1>
  {{ $data }}
  <br />
  <br />
  <label>Introduzca un número</label>
  <input type="number" v-model="numero" />
  <br />
  <br />

  <!-- 1. Propiedad conmutada que nos devuelva un <h3> con colores si el número es par o es Impar  -->
  <div v-html="evaluarNumero"></div>
  <hr />

  <!-- 2. El mismo ejemplo en el mismo component, pero con un botón y método -->
  <button @click="getParImpar()">Par / Impar</button>
  <div v-html="html"></div>
  <hr />

  <!-- 3. El mismo ejemplo en el mismo component, pero con directivas. -->
  <h3 style="color: blue" v-if="numero % 2 == 0">PAR</h3>
  <h3 v-else style="color: red">IMPAR</h3>
</template>

<script>
export default {
  name: "NumeroParImpar",

  computed: {
    evaluarNumero() {
      let data = "";
      if (this.numero % 2 == 0) {
        data = "<h3 style='color:blue'>Par: " + this.numero + "</h3>";
      } else {
        data = "<h3 style='color:green'>Impar: " + this.numero + "</h3>";
      }
      return data;
    },
  },

  methods: {
    getParImpar() {
      if (this.numero % 2 == 0) {
        this.html = "<h3 style='color:green'>Par " + this.numero + "</h3>";
      } else {
        this.html += "<h3 style='color:orange'>Impar " + this.numero + "</h3>";
      }
    },
  },

  data() {
    return {
      numero: 0,
      html: "",
    };
  },
};
</script>