<script setup lang="ts">
import {reactive, computed} from "vue";

const data = reactive({
  PI: 3.14,
  radius: Math.round(Math.random() * 10)
});

const area = computed(
  (): number => data.PI * data.radius * data.radius
);

setInterval(
  (): void => {
    data.radius = Math.round(Math.random() * 10);
  },
  1000
);
</script>

<template>
  <p>半径{{ data.radius }}の円の面積を円周率{{ data.PI }}で計算すると{{ area }}となる。</p>
</template>
