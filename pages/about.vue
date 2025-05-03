<template>
  <div class="container-custom">
    <h1>O knihovně</h1>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div>
        <div class="card mb-8">
          <h2>Historie</h2>
          <p class="mb-4">
            Městská knihovna byla založena v roce 1892 jako první veřejná knihovna v regionu. Původně 
            sídlila v malé budově na náměstí a její fond čítal pouhých 500 knih.
          </p>
          <p class="mb-4">
            V průběhu let se knihovna několikrát stěhovala a rozrůstala. Významným milníkem byl rok 1974, 
            kdy byla dokončena stavba současné budovy knihovny, která je od té doby centrem kulturního života ve městě.
          </p>
          <p>
            V roce 2018 prošla knihovna rozsáhlou rekonstrukcí, při které byly modernizovány všechny prostory 
            a přibylo i nové technické vybavení. V současné době nabízí knihovna přes 100 000 knih a jiných materiálů.
          </p>
        </div>

        <div class="card">
          <h2>Poslání knihovny</h2>
          <p class="mb-4">
            Naším posláním je poskytovat kvalitní a profesionální knihovnické a informační služby všem občanům bez rozdílu.
          </p>
          <p class="mb-4">
            Snažíme se podporovat čtenářskou gramotnost, celoživotní vzdělávání a přístup k informacím 
            prostřednictvím našich sbírek, digitálních zdrojů a programů.
          </p>
          <p>
            Věříme, že knihovny hrají klíčovou roli v demokratické společnosti a jsme odhodláni sloužit 
            jako informační centrum a kulturní instituce pro celou komunitu.
          </p>
        </div>
      </div>
      
      <div>
        <div class="card mb-8">
          <h2>Kontaktní informace</h2>
          <div class="mb-6">
            <h3 class="text-lg font-medium">Adresa</h3>
            <p>Knihovní 123</p>
            <p>110 00 Praha</p>
          </div>
          
          <div class="mb-6">
            <h3 class="text-lg font-medium">Kontakt</h3>
            <p>Telefon: +420 123 456 789</p>
            <p>Email: info@knihovna.cz</p>
          </div>
          
          <div class="mb-6">
            <h3 class="text-lg font-medium">Sociální sítě</h3>
            <p>Facebook: /mestskaknihovnacz</p>
            <p>Instagram: @knihovnacz</p>
          </div>
        </div>
        
        <div class="card">
          <h2>Otevírací doba</h2>
          <div class="grid grid-cols-2 gap-2">
            <p class="font-medium">Pondělí:</p>
            <p>9:00 - 19:00</p>
            <p class="font-medium">Úterý:</p>
            <p>9:00 - 19:00</p>
            <p class="font-medium">Středa:</p>
            <p>9:00 - 19:00</p>
            <p class="font-medium">Čtvrtek:</p>
            <p>9:00 - 19:00</p>
            <p class="font-medium">Pátek:</p>
            <p>9:00 - 19:00</p>
            <p class="font-medium">Sobota:</p>
            <p>9:00 - 13:00</p>
            <p class="font-medium">Neděle:</p>
            <p>Zavřeno</p>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Map section -->
    <div class="mt-8">
      <h2>Kde nás najdete</h2>
      <div class="aspect-w-16 aspect-h-9">
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2560.9773965864315!2d14.41784057689471!3d50.07528717155129!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x470b94f4a426b8c1%3A0xd549b0a7a6f2579a!2sN%C3%A1rodn%C3%AD%20knihovna%20%C4%8Cesk%C3%A9%20republiky!5e0!3m2!1scs!2scz!4v1711304912304!5m2!1scs!2scz" 
          width="100%" 
          height="450" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy" 
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'O knihovně | Městská knihovna'
})
</script>