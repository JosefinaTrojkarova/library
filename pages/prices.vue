<template>
  <div class="container-custom">
    <h1>Ceník služeb</h1>
    
    <div class="card mb-8">
      <h2>Registrační poplatky</h2>
      <div class="overflow-x-auto">
        <table class="min-w-full bg-white">
          <thead class="bg-blue-700 text-white">
            <tr>
              <th class="py-3 px-4 text-left">Kategorie</th>
              <th class="py-3 px-4 text-right">Roční poplatek</th>
              <th class="py-3 px-4 text-left">Poznámka</th>
            </tr>
          </thead>
          <tbody class="divide-y divide-gray-200">
            <tr>
              <td class="py-3 px-4">Dospělí</td>
              <td class="py-3 px-4 text-right">200 Kč</td>
              <td class="py-3 px-4">18-65 let</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Studenti</td>
              <td class="py-3 px-4 text-right">100 Kč</td>
              <td class="py-3 px-4">Nutno doložit platný studentský průkaz</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Děti a mládež</td>
              <td class="py-3 px-4 text-right">80 Kč</td>
              <td class="py-3 px-4">Do 18 let</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Senioři</td>
              <td class="py-3 px-4 text-right">80 Kč</td>
              <td class="py-3 px-4">Nad 65 let</td>
            </tr>
            <tr>
              <td class="py-3 px-4">ZTP</td>
              <td class="py-3 px-4 text-right">Zdarma</td>
              <td class="py-3 px-4">Nutno doložit průkaz ZTP</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Rodinná registrace</td>
              <td class="py-3 px-4 text-right">300 Kč</td>
              <td class="py-3 px-4">Až 5 členů rodiny</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    
    <div class="card mb-8">
      <h2>Výpůjční služby</h2>
      <div class="overflow-x-auto">
        <table class="min-w-full bg-white">
          <thead class="bg-blue-700 text-white">
            <tr>
              <th class="py-3 px-4 text-left">Služba</th>
              <th class="py-3 px-4 text-right">Cena</th>
              <th class="py-3 px-4 text-left">Poznámka</th>
            </tr>
          </thead>
          <tbody class="divide-y divide-gray-200">
            <tr>
              <td class="py-3 px-4">Standardní výpůjčka</td>
              <td class="py-3 px-4 text-right">Zdarma</td>
              <td class="py-3 px-4">30 dní</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Prodloužení výpůjčky</td>
              <td class="py-3 px-4 text-right">Zdarma</td>
              <td class="py-3 px-4">Max. 3× po 30 dnech</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Rezervace titulu</td>
              <td class="py-3 px-4 text-right">10 Kč</td>
              <td class="py-3 px-4">Za jeden titul</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Meziknihovní výpůjční služba (MVS)</td>
              <td class="py-3 px-4 text-right">80 Kč</td>
              <td class="py-3 px-4">Za jednu knihu</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Mezinárodní MVS</td>
              <td class="py-3 px-4 text-right">300 Kč</td>
              <td class="py-3 px-4">Za jednu knihu</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    
    <div class="card mb-8">
      <h2>Sankční poplatky</h2>
      <div class="overflow-x-auto">
        <table class="min-w-full bg-white">
          <thead class="bg-blue-700 text-white">
            <tr>
              <th class="py-3 px-4 text-left">Sankce</th>
              <th class="py-3 px-4 text-right">Poplatek</th>
              <th class="py-3 px-4 text-left">Poznámka</th>
            </tr>
          </thead>
          <tbody class="divide-y divide-gray-200">
            <tr>
              <td class="py-3 px-4">Upomínka 1. stupeň</td>
              <td class="py-3 px-4 text-right">20 Kč</td>
              <td class="py-3 px-4">7 dní po termínu</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Upomínka 2. stupeň</td>
              <td class="py-3 px-4 text-right">50 Kč</td>
              <td class="py-3 px-4">14 dní po termínu</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Upomínka 3. stupeň</td>
              <td class="py-3 px-4 text-right">100 Kč</td>
              <td class="py-3 px-4">30 dní po termínu</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Předžalobní upomínka</td>
              <td class="py-3 px-4 text-right">200 Kč</td>
              <td class="py-3 px-4">60 dní po termínu</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Poškození čárového kódu</td>
              <td class="py-3 px-4 text-right">50 Kč</td>
              <td class="py-3 px-4">Za jeden kód</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Ztráta čtenářského průkazu</td>
              <td class="py-3 px-4 text-right">50 Kč</td>
              <td class="py-3 px-4">Vystavení duplikátu</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    
    <div class="card mb-8">
      <h2>Další služby</h2>
      <div class="overflow-x-auto">
        <table class="min-w-full bg-white">
          <thead class="bg-blue-700 text-white">
            <tr>
              <th class="py-3 px-4 text-left">Služba</th>
              <th class="py-3 px-4 text-right">Cena</th>
              <th class="py-3 px-4 text-left">Poznámka</th>
            </tr>
          </thead>
          <tbody class="divide-y divide-gray-200">
            <tr>
              <td class="py-3 px-4">Tisk / kopírování (A4 černobílé)</td>
              <td class="py-3 px-4 text-right">3 Kč</td>
              <td class="py-3 px-4">Za stránku</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Tisk / kopírování (A4 barevné)</td>
              <td class="py-3 px-4 text-right">10 Kč</td>
              <td class="py-3 px-4">Za stránku</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Tisk / kopírování (A3 černobílé)</td>
              <td class="py-3 px-4 text-right">6 Kč</td>
              <td class="py-3 px-4">Za stránku</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Tisk / kopírování (A3 barevné)</td>
              <td class="py-3 px-4 text-right">20 Kč</td>
              <td class="py-3 px-4">Za stránku</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Skenování</td>
              <td class="py-3 px-4 text-right">2 Kč</td>
              <td class="py-3 px-4">Za stránku</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Přístup na internet</td>
              <td class="py-3 px-4 text-right">Zdarma</td>
              <td class="py-3 px-4">Pro čtenáře max. 60 minut denně</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Přístup na internet pro neregistrované</td>
              <td class="py-3 px-4 text-right">30 Kč</td>
              <td class="py-3 px-4">30 minut</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    
    <p class="text-sm italic">Ceník je platný od 1. 1. 2025. Knihovna si vyhrazuje právo na změnu ceníku.</p>
  </div>
</template>

<script setup>
useHead({
  title: 'Ceník | Městská knihovna'
})
</script>