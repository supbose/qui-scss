<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { onMounted, onUpdated, onUnmounted } from 'vue'
onMounted(() => {
	// const divWidth = this.$refs.cssDiv.style
	// const divHeight = this.$refs.cssDiv.style
	
	// console.log(divHeight);
})
</script>

<template>
	<div class="qui-flex-row-space-around">
		<div v-for="(item, index) in 10" class="qui-flex1">
			<div :class="[`bg-blue-${item}`,`qui-text-sm`]">{{ `bg-blue-${item}` }}</div>
		</div>
	</div>

	
</template>

<style lang="scss">
// @import '../scss/index.scss';
@import '../scss/css/index.css';
.qui-divider-left {
	border-left-width: thick;
}
</style>
