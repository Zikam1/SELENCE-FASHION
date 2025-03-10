<template>
    <section class="py-10">
      <h2 class="text-3xl font-semibold text-center mb-6">Featured Categories</h2>
      <div class="container mx-auto grid grid-cols-2 md:grid-cols-4 gap-6">
        <div v-for="item in categories" :key="item.id" class="p-4 bg-gray-100 rounded-md">
          <img :src="item.image" class="w-full h-48 object-cover rounded-md" />
          <h3 class="mt-2 text-lg">{{ item.name }}</h3>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const categories = [
    { id: 1, name: "Jackets", image: "/category1.jpg" },
    { id: 2, name: "Sneakers", image: "/category2.jpg" },
    { id: 3, name: "Dresses", image: "/category3.jpg" },
    { id: 4, name: "Accessories", image: "/category4.jpg" }
  ];
  </script>
  