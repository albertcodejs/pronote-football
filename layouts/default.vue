<script setup>
function hello() {
  console.log("hello");
}
</script>

<template>
  <div>
    <header class="bg-white flex flex-row justify-between pt-2 pb-2 pl-4 pr-4">
      <div>
        <a href="#">
          <img
            class="w-12 h-12"
            src="../public/logo.png"
            alt="pronote football logo"
          />
        </a>
      </div>
      <div class="content-center">
        <i class="fa-solid fa-bars text-2xl" @click="hello()"></i>
      </div>
      <!--
      <div class="flex content-center">
        <a href="#" class="mr-1 sm:mr-4">Pronote football</a>
        <a href="#" class="sm:mr-4">Derniers matchs à noter</a>
        <a href="#" class="sm:mr-4">Joueurs</a>
        <a href="#" class="sm:mr-4">Championnat</a>
      </div> -->
    </header>
    <slot />
  </div>
</template>
