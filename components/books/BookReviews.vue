<template>
  <div class="mt-8">
    <h2 class="text-2xl font-bold mb-6">Recenze čtenářů</h2>
    
    <!-- Reviews list -->
    <div v-if="reviews.length > 0" class="mb-8">
      <div v-for="(review, index) in reviews" :key="index" class="card mb-4">
        <div class="flex justify-between items-start mb-4">
          <div>
            <h3 class="text-lg font-bold">{{ review.name }}</h3>
            <p class="text-sm text-gray-500">{{ formatDate(review.date) }}</p>
          </div>
          <div class="flex">
            <span v-for="i in 5" :key="i" class="text-xl">
              <span v-if="i <= review.rating" class="text-yellow-500">★</span>
              <span v-else class="text-gray-300">★</span>
            </span>
          </div>
        </div>
        <p>{{ review.comment }}</p>
      </div>
    </div>
    <div v-else class="card mb-8 text-center py-8">
      <p class="text-gray-500">Zatím žádné recenze. Buďte první, kdo knihu ohodnotí!</p>
    </div>
    
    <!-- Add review form -->
    <div class="card">
      <h3 class="text-xl font-bold mb-4">Přidat recenzi</h3>
      <form @submit.prevent="addReview">
        <div class="mb-4">
          <label for="name" class="block mb-1 font-medium">Jméno</label>
          <input 
            type="text" 
            id="name" 
            v-model="newReview.name"
            class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
            required
            placeholder="Vaše jméno"
          >
        </div>
        
        <div class="mb-4">
          <label class="block mb-1 font-medium">Hodnocení</label>
          <div class="flex gap-2">
            <button 
              v-for="star in 5" 
              :key="star" 
              type="button"
              @click="newReview.rating = star"
              class="text-2xl focus:outline-none"
              :class="newReview.rating >= star ? 'text-yellow-500' : 'text-gray-300'"
            >
              ★
            </button>
          </div>
        </div>
        
        <div class="mb-4">
          <label for="comment" class="block mb-1 font-medium">Recenze</label>
          <textarea 
            id="comment" 
            v-model="newReview.comment"
            class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
            rows="4"
            required
            placeholder="Napište recenzi..."
          ></textarea>
        </div>
        
        <div class="text-right">
          <button 
            type="submit" 
            class="px-4 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
            :disabled="isSubmitting"
          >
            {{ isSubmitting ? 'Odesílám...' : 'Odeslat recenzi' }}
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  bookId: {
    type: String,
    required: true
  }
})

// Get reviews from local storage or initialize empty array
const getStoredReviews = () => {
  try {
    const storedReviews = localStorage.getItem(`book_reviews_${props.bookId}`)
    return storedReviews ? JSON.parse(storedReviews) : []
  } catch (e) {
    console.error('Error retrieving reviews from localStorage', e)
    return []
  }
}

const reviews = ref(getStoredReviews())
const isSubmitting = ref(false)

const newReview = ref({
  name: '',
  rating: 0,
  comment: '',
  date: null
})

const addReview = () => {
  if (newReview.value.name && newReview.value.rating > 0 && newReview.value.comment) {
    isSubmitting.value = true
    
    setTimeout(() => {
      // Add new review with current date
      const reviewToAdd = {
        ...newReview.value,
        date: new Date()
      }
      
      // Add to reviews array
      reviews.value.unshift(reviewToAdd)
      
      // Save to local storage
      try {
        localStorage.setItem(`book_reviews_${props.bookId}`, JSON.stringify(reviews.value))
      } catch (e) {
        console.error('Error saving reviews to localStorage', e)
      }
      
      // Reset form
      newReview.value = {
        name: '',
        rating: 0,
        comment: '',
        date: null
      }
      
      isSubmitting.value = false
    }, 500)
  }
}

const formatDate = (dateString) => {
  const date = new Date(dateString)
  return new Intl.DateTimeFormat('cs-CZ', { 
    year: 'numeric', 
    month: 'long', 
    day: 'numeric' 
  }).format(date)
}
</script>