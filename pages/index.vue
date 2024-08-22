<script setup lang="ts">
const { data } = await useFetch("/api/players");
const games = await useFetch("/api/games");
</script>

<template>
  <div class="text-center text-white pt-20">
    <div class="mb-8">
      <h1 class="text-white text-2xl pb-2">Bienvenue sur Pronote Football</h1>
      <h2 class="text-white text-lg">
        Pronote Football te permet d'attribuer des notes d'après-match aux
        joueurs de ton équipe favorite.
      </h2>
      <h2 class="mt-10 text-2xl">Les derniers matchs à noter</h2>
      <h3 class="text-lg mt-8">Équipe 1 vs Équipe 2</h3>
      <h4 class="text-xs">Compétition - Stade</h4>
    </div>
    <div
      class="h-34 bg-white rounded-xl mx-auto mt-5 overflow-hidden"
      v-for="player in data"
    >
      <h3 class="text-start ml-2 pt-1 text-red-800 font-bold">
        {{ player.firstname }} {{ player.name }}
      </h3>
      <p class="text-start ml-1 text-red-800">{{ player.position }}</p>
      <div class="text-start ml-1">
        <button class="text-red-800 py-1 px-1">0</button>
        <button class="text-red-800 py-1 px-1">1</button>
        <button class="text-red-800 py-1 px-1">2</button>
        <button class="text-red-800 py-1 px-1">3</button>
        <button class="text-red-800 py-1 px-1">4</button>
        <button class="text-red-800 py-1 px-1">5</button>
        <button class="text-red-800 py-1 px-1">6</button>
        <button class="text-red-800 py-1 px-1">7</button>
        <button class="text-red-800 py-1 px-1">8</button>
        <button class="text-red-800 py-1 px-1">9</button>
        <button class="text-red-800 py-1 px-1">10</button>
      </div>
    </div>
  </div>
</template>
