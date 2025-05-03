<template>
  <footer class="bg-gray-800 text-white">
    <div class="container-custom py-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div>
          <h3 class="text-xl font-bold mb-4">Městská knihovna</h3>
          <p class="mb-4">Moderní veřejná knihovna s rozsáhlou nabídkou knih, časopisů a dalších materiálů.</p>
          <p>© {{ new Date().getFullYear() }} Městská knihovna. Všechna práva vyhrazena.</p>
        </div>
        
        <div>
          <h3 class="text-xl font-bold mb-4">Kontakt</h3>
          <p class="mb-2">Knihovní 123</p>
          <p class="mb-2">110 00 Praha</p>
          <p class="mb-2">Tel: +420 123 456 789</p>
          <p>Email: info@knihovna.cz</p>
        </div>
        
        <div>
          <h3 class="text-xl font-bold mb-4">Otevírací doba</h3>
          <div class="grid grid-cols-2 gap-1">
            <p>Pondělí:</p>
            <p>9:00 - 19:00</p>
            <p>Úterý:</p>
            <p>9:00 - 19:00</p>
            <p>Středa:</p>
            <p>9:00 - 19:00</p>
            <p>Čtvrtek:</p>
            <p>9:00 - 19:00</p>
            <p>Pátek:</p>
            <p>9:00 - 19:00</p>
            <p>Sobota:</p>
            <p>9:00 - 13:00</p>
            <p>Neděle:</p>
            <p>Zavřeno</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>