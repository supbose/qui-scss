<template>
	<div v-for="(colorItem, index) in colorName" :key="index">
		<div class="qui-flex-row-nowrap">
			<div class="qui-flex1 qui-text qui-text-center qui-text-lines-1" v-for="(item, cindex) in 10" :key="cindex">
				<div :class="[`bg-${colorItem}-${item}`]">{{ formatColor(`${colorItem}-${item}`) }}</div>
			</div>
		</div>
	</div>
</template>

<script setup>
	import { onMounted,reactive, } from "vue"
	import color from "../command/color.js"
	const colorName = reactive([
		`blue`,
		`cyan`,
		`geekblue`,
		`gold`,
		`gray`,
		`green`,
		`lime`,
		`magenta`,
		`orange`,
		`purple`,
		`red`,
		`theme`,
		`volcano`,
		`yellow`,
	])
	onMounted(() => {
		formatColor()
	
	})
	const formatColor = (v) => {
		return color[v]
	}
</script>

<style>
</style>