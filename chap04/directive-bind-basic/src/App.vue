<script setup lang="ts">
import {ref} from "vue";

const url = ref("https://vue.js.org/");
</script>

<template>
  <p><a v-bind:href="url" target="_blank">Vue.jsのサイト</a></p>
  <p><a :href="url" target="_blank">Vue.jsのサイト(省略版)</a></p>
  <p><a v-bind:href="url + 'guide/introduction.html'" target="_blank">Vue.jsのサイト</a></p>
</template>
