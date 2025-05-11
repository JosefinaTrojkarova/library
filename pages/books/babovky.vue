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
    
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <!-- Book cover and info -->
      <div class="md:col-span-1">
        <img src="https://www.databazeknih.cz/img/books/29_/293567/big_babovky-DdY-293567.png?v=1633258113" 
             alt="Bábovky" 
             class="w-full rounded-lg shadow-lg">
      </div>
      
      <!-- Book description -->
      <div class="md:col-span-2 card">
        <div class="">
          <div class="flex items-center mb-4">
          <span class="text-3xl font-bold">Bábovky</span>
          
            <div class="flex text-yellow-500 ml-4">
              <span class="text-3xl selectedStar">★</span>
              <span class="text-3xl selectedStar">★</span>
              <span class="text-3xl selectedStar">★</span>
              <span class="text-3xl selectedStar">★</span>
              <span class="text-3xl unSelectedStar">★</span>
            </div>
            <span class="text-xl ml-2 text-gray-600 ml-4">4.2/5</span>
          </div>
          <h2>Radka Třeštíková</h2>
          <h2 class="text-xl font-bold mb-3">O knize</h2>
          <div class="space-y-4 mb-6">
            <p>
              Dvanáct žen, dvanáct osudů propojených v jednom románu. Napadlo vás někdy, co se skrývá za dveřmi, jimiž každý den procházíte? 
            </p>
            <p>
              Všechno, co se opravdu stane, se děje za dveřmi domů a bytů. Vypravěčkami jsou ženy různého věku, zaměstnání a životních osudů 
              (takže opravdu každá čtenářka si najde příběh pro sebe). Některé vzpomínají, jiné žijí svůj každodenní život nebo se potýkají 
              s nečekanou situací. Probereme se spolu s nimi ze svojí letargie a budeme se radovat, když se jejich životy posunují správným směrem.
            </p>
            <p>
              Radka Třeštíková napsala soubor propojených příběhů ze současnosti, který vypráví o náhodách a krásných koincidencích, které nás 
              potkávají a mohou lidem změnit život. O setkáních, která jsme měli minout. O lásce, kterou jsme nečekali. O bolesti, k níž jsme 
              odsouzeni. Dvanáct neobyčejných příběhů o obyčejných věcech, které musí v životě řešit každý z nás.
            </p>
          </div>
        </div>
      </div>
    </div>
    <BookReviews bookId="babovky" />
  </div>
</template>
 
<style scoped lang="scss">

@use "~/assets/scss/_variables.scss" as *;

* {
  background-color: $secondaryColor;
  color: $primaryColor;
}

.card, .card * {
  background-color: $cardBgr;
} 

.selectedStar {
  color: $primaryColor;
}
.unSelectedStar {
  color: gray;
}

</style>

<script setup>

import BookReviews from '~/components/books/BookReviews.vue';

useHead({
  title: 'Bábovky - Radka Třeštíková | Městská knihovna'
})
</script>