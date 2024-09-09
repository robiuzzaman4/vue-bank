<script setup>
import { ref } from "vue";
</script>

<template>
  <section class="w-full bg-zinc-100 p-1 rounded-xl">
    <div
      class="w-full h-full bg-white p-6 rounded-lg shadow grid place-items-center gap-6"
    >
      <div class="flex items-center gap-2">
        <img
          src="../../public/vue.svg"
          alt="vue svg logo"
          class="h-6 w-6 aspect-square"
        />
        <h2
          class="text-base sm:text-xl md:text-2xl font-medium tracking-tighter"
        >
          Welcome to Vue Bank
        </h2>
      </div>
    </div>
  </section>
</template>
