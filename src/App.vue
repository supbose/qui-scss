<!--
 * @Author: supbose yshxw@qq.com
 * @Date: 2022-07-12 20:15:06
 * @LastEditors: supbose yshxw@qq.com
 * @LastEditTime: 2022-07-13 20:26:31
 * @FilePath: \qui-scss\src\App.vue
 * @Description: 
 * 
 * Copyright (c) 2022 by supbose yshxw@qq.com, All Rights Reserved. 
-->
<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { onMounted, onUpdated, onUnmounted, reactive, ref, nextTick } from "vue";
import color from "./command/color.js";
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
]);
onMounted(() => {
	formatColor()

});
const formatColor = (v) => {
	return color[v]
}

</script>

<template>
	<div v-for="(colorItem, index) in colorName" :key="index">
		<div class="qui-flex-row-space-around">
			<div v-for="(item, cindex) in 10" class="qui-flex1 qui-text qui-text-center qui-text-lines-1" :key="cindex">
				<div :class="[`bg-${colorItem}-${item}`]">
					{{ formatColor(`${colorItem}-${item}`) }}
				</div>
			</div>
		</div>
	</div>
</template>

<style lang="scss">
@import '../scss/css/index.css';
</style>
