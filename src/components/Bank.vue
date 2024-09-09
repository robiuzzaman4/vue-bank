<script setup>
import { ref, computed } from "vue";

const totalBalance = ref(100000);
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
        <h1 class="text-2xl text-center font-medium tracking-tighter">
          Acc No: VB_09092024
        </h1>
        <div class="w-full grid grid-cols-2 gap-2">
          <span class="text-xl text-center font-medium tracking-tighter">
            Total Balance: ${{ totalBalance.toLocaleString() }}
          </span>
          <span class="text-xl text-center font-medium tracking-tighter">
            Available Balance: ${{ availableBalance.toLocaleString() }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>
