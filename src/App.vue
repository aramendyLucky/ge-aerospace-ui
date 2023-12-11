<template>
  <div id="app">
    <h1>Compute Product</h1>
    <img alt="My Image" src="./assets/pexels-photo-14197334.jpeg" />

    <p>Números: {{ number1 }} y {{ number2 }}</p>
    <button @click="calcularProducto" v-if="!mostrarProducto">Calcular</button>
    <p v-if="mostrarProducto">Producto: {{ producto }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number1: 10, // Cambia este valor al primer número deseado
      number2: 5, // Cambia este valor al segundo número deseado
      mostrarProducto: false,
      producto: 0,
    };        
  },
  methods: {
    calcularProducto() {
      // Calcular el producto de dos números
      this.producto = this.number1 * this.number2;
      // Mostrar el producto y ocultar el botón
      this.mostrarProducto = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}  


</style>
