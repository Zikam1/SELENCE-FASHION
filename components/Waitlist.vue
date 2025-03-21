<template>
  <section class="flex items-center justify-center px-4 py-12 bg-gray-50">
    <div class="flex flex-col md:flex-row bg-white rounded-2xl shadow-xl p-8 md:p-12 max-w-4xl w-full gap-8">

      <!-- Left Content -->
      <div class="flex-1 flex flex-col justify-center text-center md:text-left">
        <h2 class="text-4xl font-bold mb-4 text-gray-800">Want to Join the Waitlist?</h2>
        <p class="text-gray-600 mb-6">Be the first to know when we launch. </p>
          <button
            type="submit"
            class="w-full py-3 px-4 bg-indigo-600 text-white font-semibold rounded-md hover:bg-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-300"
          >
            Go to Google Form
          </button>
        <!-- </form> -->
      </div>

      <!-- Right Image -->
      <div class="flex-1 flex justify-center items-center">
        <img
          src="../assets/waitlist.jpg"
          alt="Waitlist Illustration"
          class="rounded-xl object-cover w-full h-auto max-h-96"
        />
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')

// This will redirect the user to the Google Form when they click submit
const redirectToGoogleForm = () => {
  const formUrl = 'https://docs.google.com/forms/d/1MVkPgujjcCKfvgSramwpx9sOWIiOwhAFi6_2lBLxGlw/'
  window.open(formUrl, '_blank') // or use '_self' if you want it in same tab
}
</script>
