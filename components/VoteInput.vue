<script setup>
import { ref } from "vue";
var amount = ref(0);
</script>
<template>
  <div class="flex flex-row">
    <div class="w-1/3 m-1">
      <button @click="amount++" type="button" class="w-3/4 bg-slate-50">
        +
      </button>
    </div>
    <div class="w-1/3 m-1">
      <button @click="amount--" class="w-3/4 bg-slate-50">-</button>
    </div>
    <div class="w-1/3 m-1">
      {{ amount }}
    </div>
  </div>
</template>
