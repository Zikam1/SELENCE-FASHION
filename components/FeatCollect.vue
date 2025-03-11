<template>
  <div class="max-w-7xl mx-auto py-20 px-6">
    <!-- Featured Collections -->
    <h2 class="text-4xl font-extrabold text-gray-900 mb-12 text-center">Featured Collections</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
      <div v-for="(collection, index) in collections" :key="index" class="relative group overflow-hidden rounded-lg shadow-lg">
        <img :src="collection.image" :alt="collection.title" class="w-full h-96 object-cover transition-transform duration-500 group-hover:scale-110" />
        <div class="absolute inset-0 bg-gradient-to-b from-black/60 to-transparent flex items-end p-6 transition-opacity duration-300 group-hover:opacity-80">
          <h3 class="text-2xl font-bold text-white">{{ collection.title }}</h3>
        </div>
      </div>
    </div>

    <!-- Testimonials -->
    <div class="mt-24">
      <h2 class="text-4xl font-extrabold text-gray-900 mb-12 text-center">What Our Customers Say</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="(testimonial, index) in testimonials" :key="index" class="bg-white p-8 rounded-xl shadow-xl border border-gray-200 hover:shadow-2xl transition-all">
          <p class="text-gray-700 italic mb-6">"{{ testimonial.feedback }}"</p>
          <p class="font-semibold text-gray-900 text-right">- {{ testimonial.name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const collections = [
  { title: "Women's Collection", image: "..assets/wms.jpg" },
  { title: "Men's Collection", image: "..assets/wms.jpg" },
  { title: "Kids' Collection", image: "/wms.jpg" }
];

const testimonials = [
  { name: "Sarah M.", feedback: "I love the quality and style of the clothes. Highly recommended!" },
  { name: "John D.", feedback: "Fast delivery and great customer service. Will shop again!" },
  { name: "Emily R.", feedback: "The best place to find trendy fashion at affordable prices." }
];
</script>
