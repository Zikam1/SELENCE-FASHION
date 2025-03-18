<template>
    <section class="flex items-center justify-center px-4 py-12 bg-gray-50">
      <div class="flex flex-col md:flex-row bg-white rounded-2xl shadow-xl p-8 md:p-12 max-w-4xl w-full gap-8">
        <!-- Form Section -->
        <div class="flex-1 flex flex-col justify-center text-center md:text-left">
          <h2 class="text-4xl font-bold mb-4 text-gray-800">Want to Join the Waitlist?</h2>
          <p class="text-gray-600 mb-6">Be the first to know when we launch. Enter your email below!</p>
          <form @submit.prevent="handleSubmit" class="flex flex-col space-y-4">
            <input
              v-model="email"
              type="email"
              placeholder="Enter your email address"
              class="border border-gray-300 rounded-xl px-4 py-3 focus:ring-2 focus:ring-blue-500 focus:outline-none"
              required
            />
            <button type="submit" class="w-full py-3 px-4 bg-indigo-600 text-white font-semibold rounded-md hover:bg-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-300">
                Join Waitlist
              </button>
          </form>
          <p v-if="submitted" class="text-green-600 mt-4">Thank you for joining the waitlist!</p>
        </div>
  
        <!-- Image Section -->
        <div class="flex-1 flex justify-center items-center">
          <img src="../assets/waitlist.jpg" alt="Waitlist Illustration" class="rounded-xl object-cover w-full h-auto max-h-96">
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const email = ref('')
  const submitted = ref(false)
  
  const handleSubmit = () => {
    console.log('Email submitted:', email.value)
    submitted.value = true
    email.value = ''
  }
  </script>
  