<script setup>
import { ref } from 'vue'

// Javascript Değişkeni (State)
const email = ref('')

// Butona basınca çalışacak fonksiyon
const kayitOl = () => {
  alert(`Kayıt olunan email: ${email.value}`)
}
</script>

<template>
  <div class="space-y-8 text-center">
    
    <div class="mb-6">
      <img 
        src="/image_1.png" 
        alt="Bytes Logo" 
        class="max-w-[400px] w-full mx-auto lg:mx-10"
      />
    </div>

    <p class="text-gray-300 text-lg leading-relaxed max-w-md mx-auto lg:mx-0">
      Staying informed on the JavaScript ecosystem has never been so entertaining.
      Delivered every Tuesday and Friday, for free.
    </p>

    <div class="bg-[#1a1a1a] p-1 rounded-lg flex flex-nowrap border border-gray-700 focus-within:border-yellow-400 transition max-w-md mx-auto lg:mx-0">
      
      <input 
        v-model="email" 
        type="email" 
        placeholder="Email Address" 
        class="bg-transparent text-white p-3 flex-1 outline-none placeholder-gray-500 min-w-0"
      />
      
      <button 
        @click="kayitOl"
        class="bg-yellow-400 hover:bg-yellow-300 text-black font-bold px-6 py-3 rounded transition duration-200 whitespace-nowrap shrink-0"
      >
        GET BYTES
      </button>

    </div>

    <p class="text-gray-500 text-sm">
      Loved by <span class="text-gray-300 font-bold">187.364 developers</span>
    </p>

  </div>
</template>