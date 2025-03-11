<template>
  <div class="max-w-7xl mx-auto py-10 px-4 pb-24">
    <!-- Featured Collections -->
    <h2 class="text-3xl font-bold text-gray-900 mb-8 text-center">Featured Collections</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="(collection, index) in collections"
        :key="index"
        class="relative group overflow-hidden rounded-lg shadow-md hover:shadow-lg transition-shadow"
      >
        <img
          :src="collection.image"
          :alt="collection.title"
          class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
        />
        <div class="absolute inset-0 bg-black/30 flex items-end p-4 transition-opacity duration-300 group-hover:opacity-90">
          <h3 class="text-xl font-semibold text-white">{{ collection.title }}</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const collections = [
  { title: "Women's Collection", image: "/images/gh.jpg" }, 
  { title: "Men's Collection", image: "/images/xs.jpg" },     
  { title: "Kids' Collection", image: "/images/wer.jpg" }  ,   
];
</script>