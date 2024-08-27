<script setup lang="ts">
const { data } = await useFetch("/api/players");
</script>

<template>
  <div class="text-center text-white pt-20 mx-4">
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
      class="h-34 bg-white rounded-full py-2 mt-5 overflow-hidden"
      v-for="player in data"
    >
      <h3 class="text-center ml-2 pt-1 text-black font-bold">
        {{ player.firstname }} {{ player.name }}
      </h3>
      <p class="text-center ml-1 text-black">{{ player.position }}</p>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
        id="0"
      >
        0
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
        id="1"
      >
        1
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
        id="2"
      >
        2
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        3
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        4
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        5
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        6
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        7
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        8
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        9
      </button>
      <button
        type="button"
        class="text-black hover:bg-slate-300 rounded-full py-1 px-2"
      >
        10
      </button>
    </div>
  </div>
</template>
