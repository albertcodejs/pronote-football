<script setup lang="ts">
import { ref, onMounted } from "vue";
import type { Ref } from "vue";

let onMobile: Ref<boolean> = ref(false);
let mobileNav: Ref<boolean> = ref(false);
let windowWidth: number;

function checkScreen() {
  windowWidth = window.innerWidth;
  if (windowWidth <= 750) {
    onMobile.value = true;
  } else {
    onMobile.value = false;
    mobileNav.value = false;
  }
}

onMounted(() => {
  window.addEventListener("resize", checkScreen);
});
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
            alt="pronote-football logo"
          />
        </a>
      </div>
      <div class="content-center" v-show="onMobile">
        <i
          class="fa-solid fa-xmark text-2xl"
          v-if="onMobile && mobileNav"
          @click="mobileNav = !mobileNav"
        ></i>
        <i
          class="fa-solid fa-bars text-2xl"
          :class="{ 'icon-active': mobileNav }"
          @click="mobileNav = !mobileNav"
          v-else
        ></i>
      </div>
      <div class="content-center" v-show="!onMobile">
        <ul class="flex list-none no-underline text-sm">
          <li>
            <a href="#" class="mr-1 sm:mr-4 cursor-pointer">Notes joueurs</a>
          </li>
          <li>
            <a href="#" class="mr-1 sm:mr-4 cursor-pointer"
              >Derniers matchs à noter</a
            >
          </li>
          <li>
            <a href="#" class="mr-1 sm:mr-4 cursor-pointer">Pronote Football</a>
          </li>
          <li>
            <a href="#" class="mr-1 sm:mr-4 cursor-pointer">Connexion</a>
          </li>
        </ul>
      </div>
      <transition name="mobile-nav">
        <ul
          v-show="mobileNav"
          class="flex flex-col fixed w-full max-w-64 h-full dropdown-nav bg-white top-0 left-0 pt-5 pb-20"
        >
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="mr-1 sm:mr-4 text-black">Notes joueurs</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Derniers matchs à noter</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Pronote Football</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Connexion</a>
          </li>
        </ul>
      </transition>
    </header>
    <slot />
    <footer class="w-full bg-white h-80 mt-5 pt-4 pb-2 pl-4 pr-4">
      <div>
        <a href="#">
          <img
            class="w-20 h-20"
            src="../public/logo.png"
            alt="pronote-football logo"
          />
        </a>
      </div>
      <div>
        <ul class="bg-white flex flex-col w-full max-w-64 pt-5">
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="mr-1 sm:mr-4 text-black">Notes joueurs</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Derniers matchs à noter</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Pronote Football</a>
          </li>
          <li class="pl-2 pb-5 font-bold">
            <a href="#" class="sm:mr-4 text-black">Connexion</a>
          </li>
        </ul>
      </div>
    </footer>
  </div>
</template>
