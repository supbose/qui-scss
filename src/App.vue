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
import { onMounted, onUpdated, onUnmounted, reactive } from "vue";
const color = reactive([
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

console.log(color.length);

onMounted((v) => {
	
	setTimeout(function() {
		formatColor(v)
	}, 3000);
	
});
const formatColor=(v)=>{
	console.log(v);
	var test = document.getElementById(v)
	
	console.log(test.style);
	// var demo = window.getComputedStyle(test, null); 
	 
	//获取节点的color
	 
	 // console.log(demo);
}
</script>

<template>
	<div class="qui-text-xs" v-for="(colorItem, index) in color">
		<div class="qui-flex-row-space-around">
			<div v-for="(item, index) in 10" class="qui-flex1">
				<div :id="`bg-${colorItem}-${item}`" style="width: 20rpx;height: 30rpx;font-size: 24rpx;" :class="[`bg-${colorItem}-${item}`]">
					{{ formatColor(`bg-${colorItem}-${item}`) }}
				</div>
			</div>
		</div>
	</div>
</template>

<style lang="scss">
// @import '../scss/index.scss';
@import '../scss/css/index.css';
.qui-flex-row-space-around {
	width: 700rpx;
	height: 500rpx;
}
</style>
