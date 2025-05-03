<template>
  <div>
    <!-- Hero section -->
    <div class="bg-blue-700 text-white">
      <div class="container-custom py-16">
        <div class="max-w-3xl">
          <h1 class="text-4xl md:text-5xl font-bold mb-4">Vítejte v Městské knihovně Nové vsy u Starého města Lurunského na Moravě</h1>
          <p class="text-xl mb-8">Objevte svět knih, znalostí a inspirace v naší moderní knihovně.</p>
          <div class="space-x-4">
            <NuxtLink to="/about" class="btn bg-white text-blue-700 hover:bg-gray-100">O knihovně</NuxtLink>
            <NuxtLink to="/books" class="btn border border-white hover:bg-blue-600">Prohlédnout knihy</NuxtLink>
          </div>
        </div>
      </div>
    </div>

    <!-- Features section -->
    <div class="container-custom py-12">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="card">
          <h3 class="text-xl font-semibold mb-3">Rozsáhlá sbírka</h3>
          <p>Nabízíme tisíce knih, časopisů a dalších materiálů pro všechny věkové kategorie a zájmy.</p>
        </div>
        
        <div class="card">
          <h3 class="text-xl font-semibold mb-3">Moderní prostředí</h3>
          <p>Naše knihovna poskytuje příjemné a klidné prostory pro čtení, studium nebo relaxaci.</p>
        </div>
        
        <div class="card">
          <h3 class="text-xl font-semibold mb-3">Pravidelné akce</h3>
          <p>Pořádáme autorská čtení, workshopy a další kulturní akce pro děti i dospělé.</p>
        </div>
      </div>
    </div>

    <!-- Latest books section -->
    <div class="bg-gray-100">
      <div class="container-custom py-12">
        <h2 class="text-3xl font-bold mb-8">Vybrané knihy</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-6">
          <div v-for="id in featuredBookIds" :key="id" class="card">
            <img v-if="books && books[id]" :src="books[id].coverUrl" :alt="books[id].title" class="w-full h-64 object-cover object-center mb-4 rounded">
            <h3 v-if="books && books[id]" class="text-xl font-semibold">{{ books[id].title }}</h3>
            <p v-if="books && books[id]" class="text-gray-600 mb-2">{{ books[id].author }}</p>
            <NuxtLink :to="`/books/${id}`" class="text-blue-600 hover:text-blue-800">Více informací</NuxtLink>
          </div>
        </div>
      </div>
    </div>
    
    <!-- CTA Section -->
    <div class="container-custom py-12">
      <div class="bg-blue-600 text-white rounded-lg p-8 text-center">
        <h2 class="text-3xl font-bold mb-4">Staňte se členem naší knihovny</h2>
        <p class="text-xl mb-6">Přijďte nás navštívit a získejte přístup k tisícům knih a dalších materiálů.</p>
        <NuxtLink to="/about" class="btn bg-white text-blue-700 hover:bg-gray-100">Dozvědět se více</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
// Fetch books from JSON file
const { data: books } = await useFetch('/books.json')

// Featured book IDs to display
const featuredBookIds = ['babovky', 'tela', 'vitezove', 'kolousek']

useHead({
  title: 'Městská knihovna | Domů'
})
</script>