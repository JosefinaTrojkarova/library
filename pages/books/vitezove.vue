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
        <img src="https://www.databazeknih.cz/img/books/53_/537007/big_vitezove-54h-537007.jpg" 
             alt="Vítězové" 
             class="w-full rounded-lg shadow-lg mb-4">
        
        <div class="bg-white p-4 rounded-lg shadow mb-4">
          <h2 class="text-xl font-bold mb-2">Detaily</h2>
          <ul class="space-y-2">
            <li><span class="font-medium">Autor:</span> Frederik Backman</li>
            <li><span class="font-medium">Vydavatel:</span> Host</li>
            <li><span class="font-medium">Rok vydání:</span> 2022</li>
            <li><span class="font-medium">Počet stran:</span> 544</li>
            <li><span class="font-medium">ISBN:</span> 978-80-275-1098-8</li>
            <li><span class="font-medium">Žánr:</span> Společenské romány, Thrillery</li>
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
          <h1 class="text-3xl font-bold mb-2">Vítězové</h1>
          <div class="flex items-center mb-4">
            <div class="flex text-yellow-500">
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span>★</span>
            </div>
            <span class="ml-2 text-gray-600">4.7/5</span>
          </div>
          
          <h2 class="text-xl font-bold mb-3">O knize</h2>
          <div class="space-y-4 mb-6">
            <p>
              Závěrečná část trilogie o hokejovém městečku Medvědín od autora bestselleru Muž jménem Ove.
            </p>
            <p>
              Poté co městečko zasáhne prudká bouře, musí být většina jeho obyvatel evakuována. Někteří však v Medvědíně zůstanou a svedou o něj boj se skupinou developérů i s přírodou. Na povrch při tom vyplují dlouho pohřbená tajemství a záště, které by se možná měly nechat navždy spát.
            </p>
            <p>
              Fredrik Backman ve třetím a posledním díle série o medvědínském hokeji a jeho fanoušcích vypráví o střetu civilizace a divočiny i o tom, co společnost dokáže ospravedlnit, aby uchránila svoje děti. Je možné vyhrát boj s mocnými protivníky? A je možné z něj vyjít bez jizev na duši?
            </p>
            <p>
              Vítězové jsou strhujícím finále trilogie, které začalo knihou Medvědín a pokračovalo bestsellerem My proti vám. Backman vypráví hluboký příběh o přátelství, loajalitě a lásce v malé komunitě, která se musí naučit žít s tragédií a která z posledních sil bojuje o holé přežití.
            </p>
          </div>
          
          <h2 class="text-xl font-bold mb-3">Ukázka z knihy</h2>
          <blockquote class="italic border-l-4 border-blue-500 pl-4 py-2 mb-6">
            "Někteří lidé žijí celý život ve stejném městě, jiní se stěhují. Někteří si myslí, že to nejlepší, 
            co může člověk udělat, je zůstat, jiní považují za nejlepší odejít. Medvědín je takový, jaký je, 
            protože je tak daleko od všeho ostatního, tak izolovaný, tak uzavřený. Komunity podobné té naší 
            budí speciální druhy pocitů, zdá se, že není možné, aby v nás nevyvolaly silné emoce, tím či oním směrem."
          </blockquote>
          
          <div class="flex justify-center">
            <button class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700 transition-colors">
              Přečíst ukázku
            </button>
          </div>
        </div>
        
        <BookReviews bookId="vitezove" />
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Vítězové - Frederik Backman | Městská knihovna'
})
</script>