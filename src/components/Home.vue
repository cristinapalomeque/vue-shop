<template>
  <header class="bg-gray-800 p-5 flex justify-center items-center">
    <a href="#" class="text-white mx-9">AllProducts</a>
    <a href="#" class="text-white mx-9">Smartphones</a>
    <a href="#" class="text-white mx-9">Notebooks</a>
    <button class="text-white py-1 px-6 ml-28 bg-blue-500 rounded">Cart</button>
  </header>
  <section class="grid grid-cols-3 container mx-auto gap-6 mt-16">
    <div id="card" class="flex flex-col">
      <img :src="item.img" class="w-full" /> />
      <h3 class="text-2x1 mt-5">{{ item.name }}</h3>
      <p class="mt-2">{{ item.price }}€</p>
      <button class="text-white py-1 px-6 mt-3 w-full bg-green-500 rounded">
        Add to cart
      </button>
    </div>
    <div id="card" class="flex flex-col">
      <img :src="item.img" class="w-full" /> />
      <h3 class="text-2x1 mt-5">{{ item.name }}</h3>
      <p class="mt-2">{{ item.price }}€</p>
      <button class="text-white py-1 px-6 mt-3 w-full bg-green-500 rounded">
        Add to cart
      </button>
    </div>

    <div id="card" class="flex flex-col">
      <img :src="item.img" class="w-full" /> />
      <h3 class="text-2x1 mt-5">{{ item.name }}</h3>
      <p class="mt-2">{{ item.price }}€</p>
      <button class="text-white py-1 px-6 mt-3 w-full bg-green-500 rounded">
        Add to cart
      </button>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style></style>
