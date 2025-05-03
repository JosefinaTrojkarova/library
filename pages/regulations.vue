<template>
  <div class="container-custom">
    <h1>Řád knihovny</h1>
    
    <div class="card mb-8">
      <h2>Všeobecná ustanovení</h2>
      <ol class="list-decimal pl-5 space-y-2">
        <li>Městská knihovna je veřejná knihovna, jejímž zřizovatelem je město.</li>
        <li>Knihovna poskytuje služby všem občanům bez rozdílu věku, národnosti, vzdělání, náboženského vyznání nebo politického přesvědčení.</li>
        <li>Služby knihovny jsou poskytovány uživatelům v souladu s Knihovním zákonem č. 257/2001 Sb.</li>
        <li>Knihovna zpracovává osobní údaje uživatelů v souladu s Nařízením Evropského parlamentu a Rady (EU) 2016/679 (GDPR).</li>
      </ol>
    </div>
    
    <div class="card mb-8">
      <h2>Registrace čtenářů</h2>
      <ol class="list-decimal pl-5 space-y-2">
        <li>Čtenářem knihovny se stává fyzická osoba vydáním čtenářského průkazu na základě vyplněné přihlášky.</li>
        <li>Při registraci je čtenář povinen prokázat se platným občanským průkazem nebo jiným dokladem totožnosti.</li>
        <li>Děti do 15 let se mohou stát čtenáři se souhlasem a podpisem zákonného zástupce.</li>
        <li>Čtenářský průkaz je nepřenosný a čtenář odpovídá za jeho případné zneužití.</li>
        <li>Platnost čtenářského průkazu je jeden rok od data registrace nebo posledního prodloužení.</li>
        <li>Čtenář je povinen hlásit změnu jména, bydliště a dalších údajů uvedených v přihlášce.</li>
      </ol>
    </div>
    
    <div class="card mb-8">
      <h2>Výpůjční řád</h2>
      <ol class="list-decimal pl-5 space-y-2">
        <li>Knihy a další materiály si mohou půjčovat pouze registrovaní čtenáři s platným čtenářským průkazem.</li>
        <li>Standardní výpůjční doba je 30 dní.</li>
        <li>Maximální počet vypůjčených položek na jednoho čtenáře je 10 kusů.</li>
        <li>Výpůjční lhůtu lze prodloužit až třikrát, pokud není publikace rezervována jiným čtenářem.</li>
        <li>O prodloužení výpůjční lhůty lze požádat osobně, telefonicky, e-mailem nebo prostřednictvím online čtenářského konta.</li>
        <li>Prezenční fond (slovníky, encyklopedie, vzácné tisky) se půjčuje pouze v prostorách knihovny.</li>
        <li>Čtenář je povinen vrátit vypůjčené materiály v takovém stavu, v jakém je převzal.</li>
      </ol>
    </div>
    
    <div class="card mb-8">
      <h2>Poplatky a sankce</h2>
      <ol class="list-decimal pl-5 space-y-2">
        <li>Za překročení výpůjční lhůty je čtenář povinen zaplatit poplatky z prodlení dle platného ceníku.</li>
        <li>Čtenář je povinen nahradit ztracené nebo poškozené materiály:</li>
        <ul class="list-disc pl-8 space-y-1">
          <li>Stejným vydáním publikace</li>
          <li>Novějším vydáním publikace</li>
          <li>Finanční náhradou ve výši aktuální pořizovací ceny publikace plus manipulační poplatek</li>
        </ul>
        <li>Při opakovaném porušování knihovního řádu může být čtenáři dočasně nebo trvale omezeno právo využívat služeb knihovny.</li>
      </ol>
    </div>
    
    <div class="card mb-8">
      <h2>Pravidla chování v knihovně</h2>
      <ol class="list-decimal pl-5 space-y-2">
        <li>Čtenáři jsou povinni chovat se v prostorách knihovny tiše a ohleduplně k ostatním návštěvníkům.</li>
        <li>V prostorách knihovny je zakázáno kouřit, konzumovat alkoholické nápoje a omamné látky.</li>
        <li>Konzumace jídla je povolena pouze ve vyhrazených prostorách.</li>
        <li>V knihovně je dovoleno používat mobilní telefony pouze v tichém režimu.</li>
        <li>Do knihovny není dovoleno vstupovat se zvířaty, s výjimkou asistenčních psů.</li>
        <li>Návštěvníci knihovny jsou povinni řídit se pokyny personálu knihovny.</li>
        <li>Každý čtenář je povinen před odchodem z knihovny vrátit vypůjčené materiály z příruční knihovny na původní místo.</li>
      </ol>
    </div>
    
    <div class="card mb-8">
      <h2>Závěrečná ustanovení</h2>
      <ol class="list-decimal pl-5 space-y-2">
        <li>Výjimky z knihovního řádu může v odůvodněných případech povolit ředitel knihovny.</li>
        <li>Jakékoliv změny v knihovním řádu podléhají schválení zřizovatelem knihovny.</li>
        <li>Tento knihovní řád nabývá účinnosti dnem 1. 1. 2025.</li>
        <li>Vydáním tohoto knihovního řádu se ruší platnost předchozího knihovního řádu.</li>
      </ol>
    </div>
    
    <div class="text-right italic">
      <p>V Praze dne 1. 12. 2024</p>
      <p class="mt-4">Mgr. Jan Novák</p>
      <p>ředitel Městské knihovny</p>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Řád knihovny | Městská knihovna'
})
</script>