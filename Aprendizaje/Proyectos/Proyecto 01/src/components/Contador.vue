<template>
  <h1>Contador:</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="disminuir">Disminuir</button>
</template>

<script setup>
import { ref } from 'vue';

const contador = ref(0);
const incrementar = () => {
  contador.value++;
}

const disminuir = () => {
  contador.value--;
  if (contador.value < 0) {
    contador.value = 0;
  }
}
</script>


<style scoped>
* {
  margin: 0;
  padding: 0;
  text-align: center;
}
p {
  font-size: 25px;
  color: #281be2;
}

button {
  background-color: rgb(16, 195, 219);
  color: white;
  padding: 8px;
  margin-left: 5px;
  border: #fff;
  border-radius: 5px;
  cursor: pointer;
}
</style>
