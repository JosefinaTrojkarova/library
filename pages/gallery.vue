<template>
  <div class="container-custom">
    <h1>Galerie knihovny</h1>
    
    <div class="mb-12">
      <h2 class="mb-6">Interiér knihovny</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('interior1')">
          <img src="https://images.unsplash.com/photo-1521587760476-6c12a4b040da?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8bGlicmFyeXxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=800&q=60" 
               alt="Hlavní sál knihovny" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Hlavní sál knihovny</p>
        </div>
        
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('interior2')">
          <img src="https://images.unsplash.com/photo-1568667256549-094345857637?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NXx8bGlicmFyeXxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=800&q=60" 
               alt="Studijní oddělení" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Studijní oddělení</p>
        </div>
        
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('interior3')">
          <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8bGlicmFyeXxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=800&q=60" 
               alt="Pult s výpůjčním systémem" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Pult s výpůjčním systémem</p>
        </div>
      </div>
    </div>
    
    <div class="mb-12">
      <h2 class="mb-6">Akce v knihovně</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('event1')">
          <img src="https://images.unsplash.com/photo-1519682337058-a94d519337bc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTF8fGxpYnJhcnklMjBldmVudHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=800&q=60" 
               alt="Autorské čtení" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Autorské čtení - Alena Mornštajnová (říjen 2024)</p>
        </div>
        
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('event2')">
          <img src="https://images.unsplash.com/photo-1517457373958-b7bdd4587205?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTd8fGxpYnJhcnklMjBldmVudHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=800&q=60" 
               alt="Workshop pro děti" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Workshop pro děti - Pohádkový svět (září 2024)</p>
        </div>
        
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('event3')">
          <img src="https://images.unsplash.com/photo-1529704693195-d9d5d4c0e8f0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGxpYnJhcnklMjBldmVudHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=800&q=60" 
               alt="Beseda s historikem" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Beseda s historikem - Dějiny Prahy (srpen 2024)</p>
        </div>
      </div>
    </div>
    
    <div class="mb-12">
      <h2 class="mb-6">Dětské oddělení</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('kids1')">
          <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTR8fGxpYnJhcnklMjBraWRzfGVufDB8fDB8fHww&auto=format&fit=crop&w=800&q=60" 
               alt="Dětský koutek" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Dětský koutek</p>
        </div>
        
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('kids2')">
          <img src="https://images.unsplash.com/photo-1529390079861-591de354faf5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjR8fGxpYnJhcnklMjBraWRzfGVufDB8fDB8fHww&auto=format&fit=crop&w=800&q=60" 
               alt="Čtení pro děti" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Čtení pro děti</p>
        </div>
        
        <div class="card p-2 hover:shadow-lg transition-shadow cursor-pointer" @click="openImage('kids3')">
          <img src="https://images.unsplash.com/photo-1588072432836-e10032774350?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8Y2hpbGRyZW4lMjByZWFkaW5nfGVufDB8fDB8fHww&auto=format&fit=crop&w=800&q=60" 
               alt="Dětská literatura" 
               class="w-full h-64 object-cover rounded">
          <p class="mt-2 text-center">Dětská literatura</p>
        </div>
      </div>
    </div>
    
    <!-- Image Lightbox -->
    <div v-if="lightboxOpen" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black bg-opacity-80" @click="closeLightbox">
      <button class="absolute top-4 right-4 text-white text-2xl" @click.stop="closeLightbox">×</button>
      <div class="max-w-4xl max-h-full" @click.stop>
        <img :src="lightboxImage" alt="Zvětšený obrázek" class="max-h-[90vh] max-w-full">
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

useHead({
  title: 'Galerie | Městská knihovna'
})

const lightboxOpen = ref(false)
const lightboxImage = ref('')

// Image mapping for gallery
const images = {
  interior1: 'https://images.unsplash.com/photo-1521587760476-6c12a4b040da?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8bGlicmFyeXxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=80',
  interior2: 'https://images.unsplash.com/photo-1568667256549-094345857637?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NXx8bGlicmFyeXxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=80',
  interior3: 'https://images.unsplash.com/photo-1507842217343-583bb7270b66?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8bGlicmFyeXxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=80',
  event1: 'https://images.unsplash.com/photo-1519682337058-a94d519337bc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTF8fGxpYnJhcnklMjBldmVudHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=80',
  event2: 'https://images.unsplash.com/photo-1517457373958-b7bdd4587205?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTd8fGxpYnJhcnklMjBldmVudHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=80',
  event3: 'https://images.unsplash.com/photo-1529704693195-d9d5d4c0e8f0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGxpYnJhcnklMjBldmVudHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=1200&q=80',
  kids1: 'https://images.unsplash.com/photo-1503676260728-1c00da094a0b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTR8fGxpYnJhcnklMjBraWRzfGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=80',
  kids2: 'https://images.unsplash.com/photo-1529390079861-591de354faf5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjR8fGxpYnJhcnklMjBraWRzfGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=80',
  kids3: 'https://images.unsplash.com/photo-1588072432836-e10032774350?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8Y2hpbGRyZW4lMjByZWFkaW5nfGVufDB8fDB8fHww&auto=format&fit=crop&w=1200&q=80'
}

const openImage = (imageId) => {
  lightboxImage.value = images[imageId]
  lightboxOpen.value = true
  document.body.style.overflow = 'hidden'
}

const closeLightbox = () => {
  lightboxOpen.value = false
  document.body.style.overflow = 'auto'
}
</script>