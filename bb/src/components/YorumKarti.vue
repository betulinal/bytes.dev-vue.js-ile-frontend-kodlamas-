<script setup>
// Dışarıdan gelecek verileri (Props) tanımlıyoruz
defineProps({
  name: String,      // Kullanıcı adı (Örn: Sdu)
  handle: String,    // Twitter kullanıcı adı (Örn: sduduzo_g)
  tweet: String,     // Yorum metni
  avatar: String,     // Profil resmi linki
  link: String
})
</script>

<template>
<a 
    :href="link" 
    target="_blank"
    class="block bg-[#161616] p-6 rounded-xl border border-gray-800 hover:border-gray-500 hover:bg-[#1f1f1f] transition duration-300 cursor-pointer group"
  >
    
<div class="flex items-center gap-3 mb-3">
      <img :src="avatar" class="w-10 h-10 rounded-full bg-gray-700 object-cover" />
      <div>
        <h3 class="font-bold text-white text-sm group-hover:text-yellow-400 transition">{{ name }}</h3>
        <p class="text-gray-400 text-xs">@{{ handle }}</p>
      </div>
      
      <div class="ml-auto text-gray-500 group-hover:text-blue-400 transition">
        <svg fill="currentColor" class="w-4 h-4" viewBox="0 0 24 24"><path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/></svg>
      </div>
    </div>

    <p class="text-gray-300 text-sm leading-relaxed">
      {{ tweet }}
    </p>

  </a>
</template>