﻿Egyiptom Tailwind Projekt
Mi az a Tailwind CSS?
A Tailwind CSS egy utility-first CSS keretrendszer, amely előre definiált osztályokat biztosít az egyes stílusok gyors alkalmazására. Például: text-center, bg-red-500, flex.
Minden stílus egy-egy apró építőelem (utility class), amelyeket kombinálva teljes designt lehet létrehozni. Ahelyett, hogy minden stílust külön CSS fájlba írnánk, a HTML kódon belül alkalmazzuk az osztályokat.
Miért érdemes használni?
Gyors fejlesztés: Az előre definiált osztályokkal az oldal felépítése gyorsabb, mint egyedi CSS írással.
Testreszabhatóság: Könnyen módosítható színek, betűtípusok, méretek, stb.
Kis méret: Csak a használt osztályok kerülnek be az elkészült CSS fájlba (purge CSS).
Tailwind CSS: 
<div class="text-center bg-red-500 p-4"></div>
Hogyan működik a Tailwind CSS?
Utility Classes
Minden osztály egy adott CSS tulajdonságot definiál.
Példa:
Színek: text-red-500, bg-blue-200.
Távolságok: m-4 (margin), p-2 (padding).
Példa HTML-ben
<div class="text-center bg-blue-500 text-white p-4 rounded-lg">
  Tailwind példaszöveg
</div>
Tailwind működési folyamata
A Tailwind CSS több ezer utility osztályt biztosít alapértelmezés szerint. Ezeket a projekthez szükséges stílusokhoz használjuk. A végleges CSS fájl csak a ténylegesen használt osztályokat tartalmazza (Purge CSS).
Tailwind CSS támogatja a reszponzív design-t breakpoint prefixekkel:
sm: (kisebb képernyők).
md:, lg:, xl: (nagyobb képernyők).
Példa:
<div class="bg-blue-500 md:bg-green-500 lg:bg-red-500">
  Reszponzív háttérszín
</div>
Állapotok (Pseudo Classes)
Tailwind támogatja az interakciós állapotokat:
Hover: hover:.
Fókusz: focus:.
Példa:
<button class="bg-blue-500 hover:bg-blue-700 text-white py-2 px-4">
  Hover színváltozás
</button>
Alapvető Tailwind CSS Osztályok
Színek
Háttérszínek: bg-blue-500, bg-red-200.
Szövegszínek: text-gray-800, text-white.
Távolságok
Margin: m-4, mx-auto (középre igazítás vízszintesen).
Padding: p-2, py-4.
Méret
Szélesség: w-1/2 (a konténer fele).
Magasság: h-screen (teljes képernyő magasság).
Tailwind Testreszabása
Config Fájl (tailwind.config.js)
Egyedi beállításokhoz testreszabhatjuk a Tailwind CSS-t.
Példa: Egyedi szín hozzáadása
javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        customBlue: '#1E40AF',
      },
    },
  },
};
HTML használat:
<div class="bg-customBlue text-white p-4">
  Egyedi szín
</div>
Tailwind CSS Gyakorlatok
Példák a gyakorlatban
Egyszerű Kártya:
<div class="max-w-sm bg-white shadow-lg rounded-lg p-4">
  <h2 class="text-xl font-bold mb-2">Kártya címe</h2>
  <p class="text-gray-600">Ez egy egyszerű kártya példa.</p>
</div>
Reszponzív Layout Grid-el:
<div class="grid grid-cols-2 gap-4 md:grid-cols-4">
  <div class="bg-blue-500 h-32"></div>
  <div class="bg-green-500 h-32"></div>
  <div class="bg-red-500 h-32"></div>
  <div class="bg-yellow-500 h-32"></div>
</div>

