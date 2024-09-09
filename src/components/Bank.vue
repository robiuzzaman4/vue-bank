<script setup>
import { ref, computed } from "vue";

const totalBalance = ref(1009000);
const accountCharge = computed(() => (totalBalance.value * 1.5) / 100); // 2.5% of the total
const availableBalance = computed(
  () => totalBalance.value - accountCharge.value
);
</script>

<template>
  <!-- container -->
  <div class="w-full max-w-screen-sm mx-auto px-4 py-12">
    <!-- balance section -->
    <div class="w-full bg-zinc-100 p-1 rounded-xl">
      <div
        class="w-full h-full bg-white p-6 rounded-lg shadow grid place-items-center gap-6"
      >
        <h1 class="text-2xl sm:text-3xl text-center font-medium tracking-tighter border-b border-b-zinc-200 w-full pb-6">
          Acc No: VB_09092024
        </h1>
        <div class="w-full flex items-center justify-between gap-2">
          <span
            class="text-base sm:text-xl md:text-2xl font-medium tracking-tighter flex flex-col gap-1"
          >
            Total Balance:
            <p class="text-emerald-500">${{ totalBalance.toLocaleString() }}</p>
          </span>
          <span class="text-base sm:text-xl md:text-2xl font-medium tracking-tighter flex flex-col gap-1">
            Available Balance:
            <p class="text-orange-500">${{ availableBalance.toLocaleString() }}</p>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>
