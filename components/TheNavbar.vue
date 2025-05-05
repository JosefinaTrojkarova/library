<template>
  <nav class="bg-blue-700 text-white shadow-md">
    <div class="container-custom py-4">
      <div class="flex justify-between items-center">
        <div class="flex items-center space-x-4">
          <img src="../images/knihyV20.25x.png" class="logo"></img>
          <NuxtLink to="/" class="text-2xl font-bold">Městská knihovna</NuxtLink>
        </div>
        
        
        <div class="hidden md:flex space-x-6">
          <NuxtLink to="/" class="hover:text-blue-200 transition-colors">Domů</NuxtLink>
          <NuxtLink to="/about" class="hover:text-blue-200 transition-colors">O knihovně</NuxtLink>
          <NuxtLink to="/gallery" class="hover:text-blue-200 transition-colors">Galerie</NuxtLink>
          <NuxtLink to="/regulations" class="hover:text-blue-200 transition-colors">Řád knihovny</NuxtLink>
          <NuxtLink to="/prices" class="hover:text-blue-200 transition-colors">Ceník</NuxtLink>
          <NuxtLink to="/books" class="hover:text-blue-200 transition-colors">Knihy</NuxtLink>
        </div>
        
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden">
          <span v-if="!isMenuOpen">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </span>
          <span v-else>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </span>
        </button>
      </div>
      
      <!-- Mobile menu -->
      <div v-if="isMenuOpen" class="md:hidden pt-4 pb-2 space-y-3">
        <NuxtLink to="/" class="block hover:text-blue-200 transition-colors">Domů</NuxtLink>
        <NuxtLink to="/about" class="block hover:text-blue-200 transition-colors">O knihovně</NuxtLink>
        <NuxtLink to="/gallery" class="block hover:text-blue-200 transition-colors">Galerie</NuxtLink>
        <NuxtLink to="/regulations" class="block hover:text-blue-200 transition-colors">Řád knihovny</NuxtLink>
        <NuxtLink to="/prices" class="block hover:text-blue-200 transition-colors">Ceník</NuxtLink>
        <NuxtLink to="/books" class="block hover:text-blue-200 transition-colors">Knihy</NuxtLink>
      </div>
    </div>
  </nav>
</template>

<script setup>
const isMenuOpen = ref(false)
</script>

<style scoped lang="scss">

  @use "~/assets/scss/_variables.scss" as *;

  * {
    background-color: $primaryColor;
    color: $secondaryColor;
  }

  .logo {
    height: 5rem;
  }
</style>