<template>
    <section class="py-10">
      <h2 class="text-3xl font-semibold text-center mb-6">Trending Now</h2>
      <div class="container mx-auto grid grid-cols-2 md:grid-cols-4 gap-6">
        <div v-for="item in products" :key="item.id" class="p-4 bg-gray-100 rounded-md">
          <img :src="item.image" class="w-full h-48 object-cover rounded-md" />
          <h3 class="mt-2 text-lg">{{ item.name }}</h3>
          <p class="text-red-500 font-semibold">${{ item.price }}</p>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const products = [
    { id: 1, name: "Stylish Jacket", price: 49.99, image: "/product1.jpg" },
    { id: 2, name: "Cool Sneakers", price: 79.99, image: "/product2.jpg" },
    { id: 3, name: "Casual Dress", price: 59.99, image: "/product3.jpg" },
    { id: 4, name: "Trendy Shirt", price: 29.99, image: "/product4.jpg" }
  ];
  </script>