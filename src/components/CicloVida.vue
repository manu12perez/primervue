<template>
  <div>
    <h1 style="color: purple">Cilos de Vida Events</h1>
    <button @click="cambiarSaludo()">Cambiar saludo</button>
    <h2>{{ saludo }}</h2>
  </div>
</template>

<script>
export default {
  name: "CicloVida",

  data() {
    return {
      saludo: "Hoy es lunes...",
    };
  },

  //   METODOS
  methods: {
    //EN ESTA ZONA INCLUIREMOS NUESTROS METODOS PERSONALIZADOS
    cambiarSaludo() {
      //SE UTILIZA LA PLABRA CLAVE this  PARA LLAMAR A LA VARIABLES DE data()
      this.saludo = "Y mañana es martes...";
    },
  },
  
  //   EVENTOS
  mounted() {
    console.log("Componente Montado");
  },
  unmounted() {
    console.log("Componente Destruido");
  },
  updated() {
    console.log("Componente Modificado");
  },
  created() {
    console.log("Componente Creado");
  },
};
</script>