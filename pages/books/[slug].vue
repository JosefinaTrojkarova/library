<template>
  <div class="container-custom">
    <div class="mb-4">
      <NuxtLink to="/books" class="text-blue-600 hover:text-blue-800 flex items-center">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
        </svg>
        Zpět na seznam knih
      </NuxtLink>
    </div>
    
    <div v-if="book" class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <!-- Book cover and info -->
      <div class="md:col-span-1">
        <img :src="book.coverUrl" 
             :alt="book.title" 
             class="w-full rounded-lg shadow-lg mb-4">
        
        <div class="bg-white p-4 rounded-lg shadow mb-4">
          <h2 class="text-xl font-bold mb-2">Detaily</h2>
          <ul class="space-y-2">
            <li><span class="font-medium">Autor:</span> {{ book.author }}</li>
            <li><span class="font-medium">Vydavatel:</span> {{ book.publisher }}</li>
            <li><span class="font-medium">Rok vydání:</span> {{ book.year }}</li>
            <li><span class="font-medium">Počet stran:</span> {{ book.pages }}</li>
            <li><span class="font-medium">ISBN:</span> {{ book.isbn }}</li>
            <li><span class="font-medium">Žánr:</span> {{ book.genres.join(', ') }}</li>
          </ul>
        </div>
        
        <div class="bg-white p-4 rounded-lg shadow">
          <h2 class="text-xl font-bold mb-2">Dostupnost</h2>
          <p class="text-green-600 mb-2" v-if="book.inStock">Na skladě</p>
          <p class="text-red-600 mb-2" v-else>Momentálně nedostupné</p>
          <p class="mb-4">Kniha je k dispozici k zapůjčení v naší knihovně.</p>
          <button class="w-full bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700 transition-colors">
            Rezervovat
          </button>
        </div>
      </div>
      
      <!-- Book description -->
      <div class="md:col-span-2">
        <div class="bg-white p-6 rounded-lg shadow">
          <h1 class="text-3xl font-bold mb-2">{{ book.title }}</h1>
          <div class="flex items-center mb-4">
            <div class="flex text-yellow-500">
              <span v-for="star in 5" :key="`full-${star}`" :class="star <= Math.floor(book.rating) ? 'text-yellow-500' : 'text-gray-300'">★</span>
            </div>
            <span class="ml-2 text-gray-600">{{ book.rating }}/5</span>
          </div>
          
          <h2 class="text-xl font-bold mb-3">O knize</h2>
          <div class="space-y-4 mb-6">
            <p v-for="(paragraph, i) in book.description" :key="i">
              {{ paragraph }}
            </p>
          </div>
          
          <h2 class="text-xl font-bold mb-3">Ukázka z knihy</h2>
          <blockquote class="italic border-l-4 border-blue-500 pl-4 py-2 mb-6">
            "{{ book.quote }}"
          </blockquote>
          
          <div class="flex justify-center">
            <button class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700 transition-colors">
              Přečíst ukázku
            </button>
          </div>
        </div>
        
        <BookReviews :bookId="book.id" />
      </div>
    </div>
    
    <div v-else class="text-center py-12">
      <h1 class="text-2xl font-bold mb-4">Kniha nenalezena</h1>
      <p>Omlouváme se, požadovaná kniha nebyla nalezena.</p>
      <NuxtLink to="/books" class="text-blue-600 hover:text-blue-800 mt-4 inline-block">
        Zpět na seznam knih
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
const route = useRoute()
const slug = route.params.slug

// Fetch data from the JSON file
const { data: books } = await useFetch('/books.json')
const book = computed(() => books.value?.[slug] || null)

// Set page title dynamically
useHead(() => ({
  title: book.value ? `${book.value.title} - ${book.value.author} | Městská knihovna` : 'Kniha nenalezena | Městská knihovna'
}))
</script>