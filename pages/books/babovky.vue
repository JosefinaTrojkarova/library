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
        <img src="https://www.databazeknih.cz/img/books/31_/319515/babovky-kPs-319515.jpg" 
             alt="Bábovky" 
             class="w-full rounded-lg shadow-lg mb-4">
        
        <div class="bg-white p-4 rounded-lg shadow mb-4">
          <h2 class="text-xl font-bold mb-2">Detaily</h2>
          <ul class="space-y-2">
            <li><span class="font-medium">Autor:</span> Radka Třeštíková</li>
            <li><span class="font-medium">Vydavatel:</span> Motto</li>
            <li><span class="font-medium">Rok vydání:</span> 2016</li>
            <li><span class="font-medium">Počet stran:</span> 264</li>
            <li><span class="font-medium">ISBN:</span> 978-80-267-0592-2</li>
            <li><span class="font-medium">Žánr:</span> Česká próza, Romány pro ženy</li>
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
          <h1 class="text-3xl font-bold mb-2">Bábovky</h1>
          <div class="flex items-center mb-4">
            <div class="flex text-yellow-500">
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span class="text-gray-300">★</span>
            </div>
            <span class="ml-2 text-gray-600">4.2/5</span>
          </div>
          
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
          
          <h2 class="text-xl font-bold mb-3">Ukázka z knihy</h2>
          <blockquote class="italic border-l-4 border-blue-500 pl-4 py-2 mb-6">
            "Koláče, bábovky, kynuté buchty. Díky své mámě jsem se v nich našla. Našla jsem v nich útěchu a nakonec i lásku. 
            Pečení se pro mě stalo vším, není to jenom koníček, je to způsob života. To, co do jídla dáváte, se vám pak vrátí. 
            Pečení je radost a radost vždycky zvítězí. I když to občas vypadá, že už je všechno prohrané."
          </blockquote>
          
          <div class="flex justify-center">
            <button class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700 transition-colors">
              Přečíst ukázku
            </button>
          </div>
        </div>
        
        <BookReviews bookId="babovky" />
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Bábovky - Radka Třeštíková | Městská knihovna'
})
</script>