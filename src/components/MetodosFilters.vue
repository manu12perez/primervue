<template>
  <div>
    <h1>Métodos Filters</h1>
    <ul>
      <li v-for="num in numeros" :key="num">
        Número: {{ num }}, Doble: {{ $filters.getNumeroDoble(num) }}
      </li>
    </ul>
    <ul>
      <li v-for="name in nombres" :key="name">
        Nombre: {{ name }}, Nombre Mayus: {{ $filters.mayuscula(name) }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MetodosFilters",

  data() {
    return {
      numeros: [12, 15, 48, 54, 78, 93, 137],
      nombres: ["Adrian", "Lucía", "Diana", "Carlos", "Antonia", "Jose", "Pepe"],
    };
  },
};
</script>