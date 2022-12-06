<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { ref } from "vue";
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";

const beers = ref([]);

async function getBeer() {
  const res = await fetch("https://api.punkapi.com/v2/beers");
  const finalRes = await res.json();
  beers.value = finalRes;
  console.log(beers.value);
}
getBeer();
</script>

<template>
  <Header />
  <section class="grid grid-cols-3 container mx-auto gap-6 mt-16">
    <Card v-for="beer in beers" :item="beer"></Card>
  </section>
</template>

<style scoped></style>
