<template>
  <header class="bg-gray-800 p-5 flex justify-center items-center">
    <a href="#" class="text-white mx-9">AllProducts</a>
    <a href="#" class="text-white mx-9">Smartphones</a>
    <a href="#" class="text-white mx-9">Notebooks</a>
    <button class="text-white py-1 px-6 ml-28 bg-blue-500 rounded">
      Cart {{ coses.length }}
    </button>
  </header>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps(["coses"]);
</script>

<style></style>
