<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <div id="app">
    <h1 style="color: #006400">Adopta un animal</h1>
    <p style="color: #458728">Estos son algunos de los animales que buscan un hogar:</p>
    <ul>
      <li v-for="animal in animals" :key="animal.id" style="color: #D0DB61">
        {{ animal.name }} - {{ animal.type }} - {{ animal.age }} años
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      animals: [
        { id: 1, name: "Luna", type: "Perro", age: 2 },
        { id: 2, name: "Simba", type: "Gato", age: 3 },
        { id: 3, name: "Kiwi", type: "Loro", age: 1 },
      ],
    };
  },
};
</script>

<style>
body {
  background-color: #FEFCD0;
  font-family: Arial, sans-serif;
}
</style>

