<script setup lamg="ts">
import {ref} from "vue";

const mousePointerX = ref(0);
const mousePointerY = ref(0);
const onImageMousemove = (event: MouseEvent): void => {
	mousePointerX.value = event.offsetX;
	mousePointerY.value = event.offsetY;
};
</script>

<template>
	<section>
		<img src="./assets/logo.svg" alt="vueのロゴ" width="200" height="200" v-on:mousemove="onImageMousemove">
		<p>ポインタの位置: x={{mousePointerX}}; y={{mousePointerY}}</p>
	</section>
</template>

<!-- 
<script setup lang="ts">
import {ref} from "vue";

const mousePointerX = ref(0);
const mousePointerY = ref(0);
const onImgMousemove = (event: MouseEvent): void => {
	mousePointerX.value = event.offsetX;
	mousePointerY.value = event.offsetY;
};
</script>

<template>
	<section>
		<img src="./assets/logo.svg" alt="Vueのロゴ" width="200" v-on:mousemove="onImgMousemove">
		<p>ポインタの位置: x={{mousePointerX}}; y={{mousePointerY}}</p>
	</section>
</template> -->
