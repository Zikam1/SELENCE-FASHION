<template>
    <section class="py-10">
      <h2 class="text-3xl font-semibold text-center mb-6">What Customers Say</h2>
      <div class="container mx-auto grid md:grid-cols-3 gap-6">
        <div v-for="testimonial in testimonials" :key="testimonial.id" class="p-6 bg-gray-100 rounded-md">
          <p class="text-lg italic">"{{ testimonial.review }}"</p>
          <h4 class="mt-2 font-semibold">{{ testimonial.name }}</h4>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const testimonials = [
    { id: 1, name: "John Doe", review: "Amazing products, fast delivery!" },
    { id: 2, name: "Jane Smith", review: "Love the quality and service!" },
    { id: 3, name: "Alice Brown", review: "Great fashion at great prices!" }
  ];
  </script>
  