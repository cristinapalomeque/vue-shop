<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { ref } from "vue";

const product = ref({
  img: "https://images-americanas.b2w.io/produtos/01/00/item/132381/3/132381386G1.png",
  name: "Notebook Lenovo",
  price: 100,
});
</script>

<template>
  <div class="card">
    <img v-bind:src="product.img" />
    <a href="">{{ product.name }}</a>
    <p>{{ product.price }}€</p>
    <button>Add to cart</button>
  </div>
</template>

<style scoped></style>
