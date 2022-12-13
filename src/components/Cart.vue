<template>
  <div class="box-border p-4 border-4 bg-white absolute top-0 right-0">
    <div v-for="product in products" class="flex flex-row">
      <img class="object-cover h-28 w-76" :src="product.image_url" />
      <div>
        <div>{{ product.name }}</div>
        <div>1</div>
        <div>{{ product.ibu }}</div>
      </div>
    </div>
    <div>Total: {{ totalPrice }}</div>
  </div>
</template>

<script setup>
import { computed } from "vue";
const props = defineProps(["products"]);

const totalPrice = computed(() => {
  return props.products.reduce((acc, product) => acc + product.ibu, 0);
});
</script>

<style scoped></style>
