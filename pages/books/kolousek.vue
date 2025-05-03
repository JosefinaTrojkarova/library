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
        <img src="https://www.databazeknih.cz/img/books/52_/525478/big_kolousek-aOB-525478.jpg" 
             alt="Koloušek" 
             class="w-full rounded-lg shadow-lg mb-4">
        
        <div class="bg-white p-4 rounded-lg shadow mb-4">
          <h2 class="text-xl font-bold mb-2">Detaily</h2>
          <ul class="space-y-2">
            <li><span class="font-medium">Autor:</span> Jana Bernášková</li>
            <li><span class="font-medium">Vydavatel:</span> CPress</li>
            <li><span class="font-medium">Rok vydání:</span> 2022</li>
            <li><span class="font-medium">Počet stran:</span> 304</li>
            <li><span class="font-medium">ISBN:</span> 978-80-264-4044-9</li>
            <li><span class="font-medium">Žánr:</span> Psychologické romány, Česká próza</li>
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
          <h1 class="text-3xl font-bold mb-2">Koloušek</h1>
          <div class="flex items-center mb-4">
            <div class="flex text-yellow-500">
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span>★</span>
              <span class="text-gray-300">★</span>
            </div>
            <span class="ml-2 text-gray-600">4.1/5</span>
          </div>
          
          <h2 class="text-xl font-bold mb-3">O knize</h2>
          <div class="space-y-4 mb-6">
            <p>
              Pokud se Linda vydá na dovolenou se svým manželem a jeho dcerou z prvního manželství, nejspíš už tuší, že to nebude idylka. Netuší ale, jak moc dokáže jedna osudová návštěva změnit její život.
            </p>
            <p>
              Linda se vydává na dovolenou se svým manželem a jeho dcerou z prvního manželství. Už od začátku je jasné, že cesta klidu a míru se nekoná, a pak se objeví nečekaná návštěva. Krásná mladá dívka, která se představí jako Adéla, se zprvu zdá jako rozpustilá holka, která ze sebe jen tak sype historky o svém životě. Jenže postupně se ukáže, že skutečnost je jiná.
            </p>
            <p>
              Prvoplánově slunná dovolená se mění v psychologický thriller, ve kterém vystupují na povrch nejenom nenaplněné erotické touhy a pokřivená sexualita, ale i dětská traumata a nezvládnutá agrese.
            </p>
            <p>
              Koloušek je strhující, hluboce znepokojivý, ale zároveň velice terapeutický román, kde se napínavý příběh snoubí s jazykem plným smyslnosti a otevřenosti. Jana Bernášková dává čtenáři nahlédnout do zákulisí dysfunkčního manželství, do nezhojených dětských ran a do destruktivních emočních vzorců, s nimiž se postava Lindy snaží poprat. Držíte v rukou velký román o současnosti a o lásce ve všech jejích podobách.
            </p>
          </div>
          
          <h2 class="text-xl font-bold mb-3">Ukázka z knihy</h2>
          <blockquote class="italic border-l-4 border-blue-500 pl-4 py-2 mb-6">
            "Málokdo si uvědomuje, kolik násilí je ve vzduchu, který dýcháme, v obyčejných každodenních situacích. 
            A to proto, že jsme si na něj zvykli. Vlastně ani nevnímáme, že umýt nádobí po večeři má být samozřejmostí ženy, 
            že vystoupit do kopce a nechat muže v autě u řízení je projevem slabosti, že pokud muž nevysvětlí, 
            proč dělá to, co dělá, je to proto, že se své ženě zpovídat nemusí. Cvak. Necvak."
          </blockquote>
          
          <div class="flex justify-center">
            <button class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700 transition-colors">
              Přečíst ukázku
            </button>
          </div>
        </div>
        
        <BookReviews bookId="kolousek" />
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Koloušek - Jana Bernášková | Městská knihovna'
})
</script>