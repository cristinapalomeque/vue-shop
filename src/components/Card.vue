<template>
  <div id="card" class="flex flex-col">
    <img :src="item.image_url" class="w-full h-[250px] object-cover" />
    <h3 class="text-2x1 mt-5">{{ item.name }}</h3>
    <p class="mt-2">{{ item.ibu }}€</p>
    <button
      class="text-white py-1 px-6 mt-3 w-full bg-green-500 rounded"
      v-on:click="addToCart()"
    >
      Add to cart
    </button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps(["item"]);

function addToCart() {
  // emit event (item)
}
</script>

<style></style>
