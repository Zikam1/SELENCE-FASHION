<template>
  <div class="py-16 bg-gray-50">
    <div class="container mx-auto px-6 md:px-12 lg:px-20 text-center">
      <h2 class="text-4xl font-bold text-gray-900 mb-12">
        What Our Customers Say
      </h2>

      <div class="relative w-full max-w-4xl mx-auto">
        <!-- Carousel Wrapper -->
        <div class="overflow-hidden relative">
          <div 
            class="flex transition-transform duration-500 ease-in-out"
            :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
          >
            <div 
              v-for="(testimonial, index) in testimonials" 
              :key="index"
              class="min-w-full px-6"
            >
              <div class="bg-white p-8 rounded-xl shadow-md border border-gray-200">
                <p class="text-gray-600 italic text-lg mb-4">
                  "{{ testimonial.feedback }}"
                </p>
                <div class="flex items-center justify-center gap-4">
                  <img 
                    :src="testimonial.image"
                    :alt="testimonial.name"
                    class="w-12 h-12 rounded-full object-cover border-2 border-indigo-600"
                  />
                  <p class="font-semibold text-gray-900">{{ testimonial.name }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Navigation Buttons -->
        <button 
          @click="prevSlide" 
          class="absolute left-0 top-1/2 transform -translate-y-1/2 bg-indigo-600 text-white p-3 rounded-full shadow-md hover:bg-indigo-700 transition"
        >
          ❮
        </button>
        <button 
          @click="nextSlide" 
          class="absolute right-0 top-1/2 transform -translate-y-1/2 bg-indigo-600 text-white p-3 rounded-full shadow-md hover:bg-indigo-700 transition"
        >
          ❯
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const testimonials = ref([
  { name: "Sarah M.", feedback: "Absolutely love the quality! Will definitely shop again.", image: "https://randomuser.me/api/portraits/women/1.jpg" },
  { name: "John D.", feedback: "Great service and fast delivery! Highly recommended.", image: "https://randomuser.me/api/portraits/men/2.jpg" },
  { name: "Emily R.", feedback: "Trendy fashion at the best prices. Love it!", image: "https://randomuser.me/api/portraits/women/3.jpg" }
]);

const currentIndex = ref(0);

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + testimonials.value.length) % testimonials.value.length;
};

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % testimonials.value.length;
};
</script>
