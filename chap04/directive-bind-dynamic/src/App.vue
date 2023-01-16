<script setup lang="ts">
import {ref} from "vue";

const widthOrHeight = ref("height");
const height = ref(100);
</script>

<template>
	<p><img alt="VueLogo" src="./assets/logo.svg" v-bind:[widthOrHeight]="height"></p>
</template>