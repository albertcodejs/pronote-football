<script setup>
import { ref } from "vue";

let mobile = true;
let mobileNav = ref(false);
</script>

<template>
  <div>
    <header
      class="fixed w-full bg-white flex flex-row justify-between pt-2 pb-2 pl-4 pr-4"
    >
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
        <i
          class="fa-solid fa-xmark text-2xl"
          v-if="mobile && mobileNav"
          @click="mobileNav = !mobileNav"
        ></i>
        <i
          class="fa-solid fa-bars text-2xl"
          :class="{ 'icon-active': mobileNav }"
          @click="mobileNav = !mobileNav"
          v-else
        ></i>
      </div>
      <ul
        class="flex content-center list-none no-underline text-xs"
        v-show="!mobile"
      >
        <li><a href="#" class="mr-1 sm:mr-4">Pronote football</a></li>
        <li><a href="#" class="mr-1 sm:mr-4">Derniers matchs à noter</a></li>
        <li><a href="#" class="mr-1 sm:mr-4">Joueurs</a></li>
        <li><a href="#" class="mr-1 sm:mr-4">Championnat</a></li>
      </ul>
      <transition name="mobile-nav">
        <ul
          v-show="mobileNav"
          class="flex flex-col fixed w-full max-w-64 h-full dropdown-nav bg-white top-0 left-0 pt-5 pb-20"
        >
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="mr-1 sm:mr-4 text-black">Pronote football</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Derniers matchs à noter</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Joueurs</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Championnat</a>
          </li>
        </ul>
      </transition>
    </header>
    <slot />
  </div>
</template>
