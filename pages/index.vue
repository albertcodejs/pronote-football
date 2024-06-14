<script setup lang="ts">
const { data } = await useFetch("/api/players");
const games = await useFetch("/api/games");
console.log("games", games);
</script>

<template>
  <div class="text-center text-white pt-10">
    <div class="mb-8">
      <h1 class="text-white text-2xl pb-2">Bienvenue sur Pronote Football</h1>
      <h2 class="text-white text-lg">
        Notez les joueurs de l'équipe de France après leurs matchs à l'euro 2024
      </h2>
      <h3 class="text-lg mt-8">Autriche - France</h3>
      <h4 class="text-xs">Euro 2024 - ESPRIT arena de Dusseldorf</h4>
    </div>
    <div
      class="w-1/2 h-34 bg-white rounded-xl mx-auto mt-5 overflow-hidden"
      v-for="player in data"
    >
      <h3 class="text-start ml-2 pt-1 text-black font-bold">
        {{ player.firstname }} {{ player.name }}
      </h3>
      <p class="text-start ml-2 text-black">{{ player.position }}</p>
      <div class="text-start ml-1">
        <button class="text-black py-1 px-1">0</button>
        <button class="text-black py-1 px-1">1</button>
        <button class="text-black py-1 px-1">2</button>
        <button class="text-black py-1 px-1">3</button>
        <button class="text-black py-1 px-1">4</button>
        <button class="text-black py-1 px-1">5</button>
        <button class="text-black py-1 px-1">6</button>
        <button class="text-black py-1 px-1">7</button>
        <button class="text-black py-1 px-1">8</button>
        <button class="text-black py-1 px-1">9</button>
        <button class="text-black py-1 px-1">10</button>
      </div>
    </div>
  </div>
</template>
