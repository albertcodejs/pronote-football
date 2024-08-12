<template>
  <div>
    <header class="flex justify-evenly pt-2 pb-2 bg-white">
      <img
        class="w-12 h-12"
        src="../public/logo.png"
        alt="pronote football logo"
      />
      <a href="#" class="content-center">Pronote football</a>
      <a href="#" class="content-center">Players</a>
      <a href="#" class="content-center">Ligue 1</a>
      <a href="#" class="content-center">Champions league</a>
    </header>
    <slot />
    <footer class="flex">
      <a class="text-white pb-2">Pronote Football</a>
      <a class="text-white pb-2">À propos</a>
      <a class="text-white pb-2">Classement Ligue 1</a>
      <a class="text-white pb-2">Classement Europe</a>
    </footer>
  </div>
</template>
