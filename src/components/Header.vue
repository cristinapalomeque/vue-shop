<template>
  <header class="bg-gray-800 p-5 flex justify-center items-center relative">
    <a href="#" class="text-white mx-9">AllProducts</a>
    <a href="#" class="text-white mx-9">Smartphones</a>
    <a href="#" class="text-white mx-9">Notebooks</a>
    <button
      @click="show = !show"
      class="text-white py-1 px-6 ml-28 bg-blue-500 rounded"
    >
      Cart {{ products.length }}
    </button>
    <Cart v-if="show" v-bind:products="products"></Cart>
  </header>
</template>

<script setup>
import { ref } from "vue";
import Cart from "./Cart.vue";

const props = defineProps(["products"]);
const show = ref(false);
</script>

<style></style>
