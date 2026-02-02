<script setup>
import GirisBolumu from './components/GirisBolumu.vue'
import YorumKarti from './components/YorumKarti.vue'

// Listeyi uzattım ki scroll çıksın ve sticky özelliği belli olsun
const tweetler = [

  { 

    id: 1, 

    name: 'Sdu', 

    handle: 'sduduzo_g', 

    tweet: 'This is the first ever newsletter that I open a music playlist for and maximize my browser just to read it in peace. Kudos for great weekly content.',

    avatar: 'https://a.storyblok.com/f/191576/1176x882/f95162c213/profile_picture_hero_before.webp' ,

    link: 'https://x.com/'

  },

  { 

    id: 2, 

    name: 'Brandon Bayer', 

    handle: 'flybayer', 

    tweet: 'The Bytes newsletter is a work of art! It’s the only dev newsletter I’m subscribed to. They somehow take semi boring stuff and infuse it with just the right amount of comedy.',

    avatar: 'https://img-s1.onedio.com/id-6899fb53bb3a0ba4b48b26ef/rev-0/w-600/h-900/f-jpg/s-89b6cd25c3c2565b779ae3ed3835fe43a6e7229b.jpg' ,

    link: 'https://x.com/'

  },

  { 

    id: 3, 

    name: 'Barbara Liau', 

    handle: 'barbaraliau', 

    tweet: 'Look forward to reading Bytes every time it drops! Funny, informative, and keeps me up to date with everything happening in the web dev world.',

    avatar: 'https://cdn.r10.net/editor/104108/1de240eeca26873334309d0acf9ba476.jpeg' ,

    link: 'https://x.com/'

  },

    { 

    id: 4, 

    name: 'Flora', 

    handle: 'flora01', 

    tweet: 'Look forward to reading Bytes every time it drops! Funny, informative, and keeps me up to date with everything happening in the web dev world.',

    avatar: 'https://preview.redd.it/is-flora-weak-v0-v7bja5dgc2id1.jpeg?auto=webp&s=1a557dc47f3a8b02253e1ed7e589e2387fa97e9c' ,

    link: 'https://x.com/'

  },

    { 

    id: 5, 

    name: 'Barbara Liau', 

    handle: 'barbaraliau', 

    tweet: 'Look forward to reading Bytes every time it drops! Funny, informative, and keeps me up to date with everything happening in the web dev world.',

    avatar: 'https://marketplace.canva.com/EAF9tfIhOlk/2/0/1600w/canva-bej-pembe-basit-profesyonel-facebook-profil-resmi-Rkv6cMhp-UI.jpg' ,

    link: 'https://x.com/'

  },

    { 

    id: 6, 

    name: 'Ricardo Quaresma', 

    handle: 'ricardo7', 

    tweet: 'Look forward to reading Bytes every time it drops! Funny, informative, and keeps me up to date with everything happening in the web dev world.',

    avatar: 'https://preview.redd.it/ricardo-quaresma-no-one-loved-me-as-much-as-be%C5%9Fikta%C5%9F-fans-v0-qym50iub2uae1.jpeg?auto=webp&s=70bdec7ea0df37ee9bb8a15eec8bfd3e1b4314de' ,

    link: 'https://twitter.com/Besiktas'

  }

]
</script>

<template>
  <div class="min-h-screen lg:h-screen bg-[#0f0f0f] text-white flex justify-center font-sans lg:overflow-hidden">
    
    <div class="max-w-6xl w-full flex flex-col lg:flex-row h-full">
      
      <div class="lg:w-1/2 w-full h-full flex flex-col justify-center p-6 lg:p-10 z-10 bg-[#0f0f0f]">
        <GirisBolumu />
      </div>

      <div class="lg:w-1/2 w-full h-full lg:overflow-y-auto scroll-smooth bg-[#0f0f0f]">
        
        <div class="space-y-5 p-6 py-10 lg:py-20">
          <YorumKarti 
            v-for="tweet in tweetler" 
            :key="tweet.id"
            :name="tweet.name"
            :handle="tweet.handle"
            :tweet="tweet.tweet"
            :avatar="tweet.avatar"
            :link="tweet.link"
          />
        </div>

      </div>

    </div>
  </div>
</template>