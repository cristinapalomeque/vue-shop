<template>
  <Header v-bind:products="products" />

  <section class="grid grid-cols-3 container mx-auto gap-6 mt-16">
    <Card
      v-for="beer in beers"
      v-bind:item="beer"
      @click="addToCart(beer)"
    ></Card>
  </section>
</template>

<script setup>
import { ref } from "vue";
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";

const beers = ref([]);
const products = ref([]);

async function getBeer() {
  const res = await fetch("https://api.punkapi.com/v2/beers");
  const finalRes = await res.json();
  beers.value = finalRes;
}
getBeer();

function addToCart(beer) {
  products.value.push(beer);
}
</script>

<style scoped></style>
