<template>
         <div class="max-w-6xl mx-auto py-16 px-4">
           <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Featured Collections</h2>
           <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
             <div class="relative">
               <img src="../assets/wms.jpg" alt="Women's Collection" class="w-full h-96 object-cover rounded-lg" />
               <div class="absolute inset-0 bg-black bg-opacity-30 flex items-center justify-center">
                 <h3 class="text-2xl font-bold text-white">Women's Collection</h3>
               </div>
             </div>
             <div class="relative">
               <img src="../assets/wms.jpg" alt="Men's Collection" class="w-full h-96 object-cover rounded-lg" />
               <div class="absolute inset-0 bg-black bg-opacity-30 flex items-center justify-center">
                 <h3 class="text-2xl font-bold text-white">Men's Collection</h3>
               </div>
             </div>
             <div class="relative">
               <img src="../assets/wms.jpg" alt="Kids' Collection" class="w-full h-96 object-cover rounded-lg" />
               <div class="absolute inset-0 bg-black bg-opacity-30 flex items-center justify-center">
                 <h3 class="text-2xl font-bold text-white">Kids' Collection</h3>
               </div>
             </div>
           </div>
      
     
         <!-- Trending Products -->
         <div class="bg-gray-100 py-16">
           <div class="max-w-6xl mx-auto px-4">
             <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Trending Products</h2>
             <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-6">
               <ProductCard v-for="product in trendingProducts" :key="product.id" :product="product" />
             </div>
           </div>
         </div>
     
         <!-- Testimonials -->
         <div class="max-w-6xl mx-auto py-16 px-4">
           <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">What Our Customers Say</h2>
           <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
             <div class="bg-white p-6 rounded-lg shadow-md">
               <p class="text-gray-600 mb-4">"I love the quality and style of the clothes. Highly recommended!"</p>
               <p class="font-semibold text-gray-800">- Sarah M.</p>
             </div>
             <div class="bg-white p-6 rounded-lg shadow-md">
               <p class="text-gray-600 mb-4">"Fast delivery and great customer service. Will shop again!"</p>
               <p class="font-semibold text-gray-800">- John D.</p>
             </div>
             <div class="bg-white p-6 rounded-lg shadow-md">
               <p class="text-gray-600 mb-4">"The best place to find trendy fashion at affordable prices."</p>
               <p class="font-semibold text-gray-800">- Emily R.</p>
             </div>
           </div>
         </div>
       </div>
   
     </template>
     
     <script setup>
     const trendingProducts = [
       { id: 1, name: "Striped T-Shirt", price: 29.99, image: "..assets/wms.jpg" },
       { id: 2, name: "Denim Jacket", price: 59.99, image: "..assets/wms.jpg" },
       { id: 3, name: "Floral Dress", price: 49.99, image: "..assets/wms.jpg" },
       { id: 4, name: "Slim Fit Jeans", price: 39.99, image: "..assets/wms.jpg" },
     ];
     </script>