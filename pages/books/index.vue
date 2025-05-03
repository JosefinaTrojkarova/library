<template>
  <div class="container-custom">
    <h1>Naše knihy</h1>
    
    <div class="mb-8">
      <p class="text-lg">Prohlédněte si výběr z našich nejnovějších knih. Kliknutím na knihu získáte více informací a můžete přidat recenzi.</p>
    </div>
    
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
      <div v-for="(book, id) in books" :key="id" class="card hover:shadow-lg transition-shadow">
        <NuxtLink :to="`/books/${id}`" class="block">
          <div class="relative">
            <img :src="book.coverUrl" 
                 :alt="book.title" 
                 class="w-full h-64 object-cover object-center rounded">
            <div class="absolute bottom-2 right-2 bg-yellow-400 text-gray-800 rounded-full w-10 h-10 flex items-center justify-center font-bold">
              {{ book.rating }}
            </div>
          </div>
          <div class="py-4">
            <h3 class="text-xl font-bold">{{ book.title }}</h3>
            <p class="text-gray-600 mb-2">{{ book.author }}</p>
            <p class="line-clamp-3 text-sm">
              {{ book.description[0] }}
            </p>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
// Fetch books from JSON file
const { data: books } = await useFetch('/books.json')

useHead({
  title: 'Knihy | Městská knihovna'
})
</script>