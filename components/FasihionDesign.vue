<template>
  <div class="py-16 bg-gray-50">
    <div class="container mx-auto px-6 md:px-12 lg:px-20">
      <h2 class="text-4xl font-bold text-gray-900 text-center mb-12">
        Discover the Latest Africa Fashion Trends
      </h2>

      <!-- Fashion Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <div 
          v-for="(fashion, index) in fashionImages" 
          :key="index" 
          class="relative group overflow-hidden rounded-lg shadow-lg cursor-pointer"
        >
          <img 
            :src="fashion.image" 
            :alt="fashion.title" 
            class="w-full h-72 object-cover transition-transform duration-300 group-hover:scale-110"
          />
          <div class="absolute inset-0 bg-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
            <h3 class="text-xl font-semibold text-white">{{ fashion.title }}</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const fashionImages = [
  { title: "Elegant Women's Wear", image: "/images/wms.jpg" },  // Local image (placed inside `/public/images/`)
  { title: "Classic Men's Fashion", image: "/images/portrait.jpg" },
  { title: "Trendy Street Style", image: "/images/man.webp" },
  { title: "Casual Summer Looks", image: "/images/mediumn.png" },
  { title: "Luxury Designer Wear", image: "/images/united.webp" },
  { title: "Stylish Accessories", image: "/images/close-.jpg" },
  { title: "Vintage Fashion", image: "/images/vibrant.webp" },
  { title: "Kids' Fashion", image: "/images/africa-kids.webp" }
];
</script>
