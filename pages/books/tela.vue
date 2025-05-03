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
        <img src="https://www.databazeknih.cz/img/books/51_/518826/big_tela-riu-518826.jpg" 
             alt="Těla" 
             class="w-full rounded-lg shadow-lg mb-4">
        
        <div class="bg-white p-4 rounded-lg shadow mb-4">
          <h2 class="text-xl font-bold mb-2">Detaily</h2>
          <ul class="space-y-2">
            <li><span class="font-medium">Autor:</span> Klára Vlasáková</li>
            <li><span class="font-medium">Vydavatel:</span> Host</li>
            <li><span class="font-medium">Rok vydání:</span> 2022</li>
            <li><span class="font-medium">Počet stran:</span> 260</li>
            <li><span class="font-medium">ISBN:</span> 978-80-275-1057-5</li>
            <li><span class="font-medium">Žánr:</span> Česká próza, Romány</li>
          </ul>
        </div>
        
        <div class="bg-white p-4 rounded-lg shadow">
          <h2 class="text-xl font-bold mb-2">Dostupnost</h2>
          <p class="text-green-600 mb-2">Na skladě</p>
          <p class="mb-4">Kniha je k dispozici k zapůjčení v naší knihovně.</p>
          <button class="w-full bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700 transition-colors">
            Rezervovat
          </button>
        </div>
      </div>
      
      <!-- Book description -->
      <div class="md:col-span-2">
        <div class="bg-white p-6 rounded-lg shadow">
          <h1 class="text-3xl font-bold mb-2">Těla</h1>
          <div class="flex items-center mb-4">
            <div class="flex text-yellow-500">
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span>★</span>
            </div>
            <span class="ml-2 text-gray-600">4.5/5</span>
          </div>
          
          <h2 class="text-xl font-bold mb-3">O knize</h2>
          <div class="space-y-4 mb-6">
            <p>
              Třicátnice Ester odchází ze slibně rozjeté kariéry v Paříži, aby se vrátila do Prahy a přispěla k vyrovnání se s temnou minulostí české společnosti.
            </p>
            <p>
              Díky práci pro dokumentaristický projekt zaměřený na připomínku zločinů komunismu se seznámí s Olinou, která ji přivede na stopu své matky a posléze i babičky. Obě byly v padesátých letech vězněny a podrobeny psychickému i fyzickému nátlaku – dokonce v rámci lékařských pokusů. Jsou to ale především tři ženy různého věku, které jsou nuceny čelit násilí pronikajícímu do jejich osobního prostoru a zároveň i jeho nečekaným následkům.
            </p>
            <p>
              Román Těla vypráví tři příběhy žen z různých časových období komunistické i české historie, které se postupně rozvíjejí, až se v závěru překvapivě spojí. Každá z hrdinek je totiž určitým způsobem poznamenána násilím a manipulací. Ester se postupně dostává hlouběji do spleti nečekaných souvislostí a poodkrývá děsivou stránku historie vlastní rodiny, která toužila především na všechno zapomenout. Text je vystavěn s citlivostí vůči jazyku a nabízí výborně zachycenou atmosféru různých období české historie včetně současnosti.
            </p>
          </div>
          
          <h2 class="text-xl font-bold mb-3">Ukázka z knihy</h2>
          <blockquote class="italic border-l-4 border-blue-500 pl-4 py-2 mb-6">
            "To ráno vstala jako obyčejně, ale něco bylo jinak. Vzpomněla si na sen, v němž se jí zdálo o těle, které mizelo pod vodou. 
            Nemohla si vybavit, jestli to bylo její tělo, nebo někoho jiného. Jediné, co si pamatovala, byl pocit oddání se 
            neúprosnému proudu, který tělo strhával ke dnu. A z toho klesání nebyla cítit úzkost, ale zvláštní, tichý klid."
          </blockquote>
          
          <div class="flex justify-center">
            <button class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700 transition-colors">
              Přečíst ukázku
            </button>
          </div>
        </div>
        
        <BookReviews bookId="tela" />
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Těla - Klára Vlasáková | Městská knihovna'
})
</script>