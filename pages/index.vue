<script>
const players = [
  {
    firstname: "Mike",
    name: "Maignan",
    position: "Gardien",
  },
];
console.log("players:", players);
</script>

<template>
  <div class="text-center text-white pt-10">
    <h1 class="text-white text-2xl pb-2">Bienvenue sur Pronote Football</h1>
    <h2 class="text-white text-lg">
      Notez les joueurs de l'équipe de France après leurs matchs à l'euro 2024
    </h2>
    <h3 class="text-lg mt-8">Autriche - France</h3>
    <h4 class="text-xs">Euro 2024 - ESPRIT arena de Dusseldorf</h4>
    <div class="bg-white w-1/2 h-14 mx-auto rounded-xl mt-8">
      <h3 class="text-start ml-2 pt-1 text-black font-bold">Mike Maignan</h3>
      <p class="text-start ml-2 text-black">Gardien</p>
      <div class="pt-1">
        <button class="text-white py-2 px-4">0</button>
        <button class="text-white py-2 px-4 ml-1">1</button>
        <button class="text-white py-2 px-4 ml-1">2</button>
        <button class="text-white py-2 px-4 ml-1">3</button>
        <button class="text-white py-2 px-4 ml-1">4</button>
        <button class="text-white py-2 px-4 ml-1">5</button>
        <button class="text-white py-2 px-4 ml-1">6</button>
        <button class="text-white py-2 px-4 ml-1">7</button>
        <button class="text-white py-2 px-4 ml-1">8</button>
        <button class="text-white py-2 px-4 ml-1">9</button>
        <button class="text-white py-2 px-4 ml-1">10</button>
      </div>
    </div>
  </div>
</template>
