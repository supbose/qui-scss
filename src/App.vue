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
import { onMounted, onUpdated, onUnmounted, reactive, ref } from "vue";
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

onMounted(() => {
});
</script>

<template>
	<div class="qui-text-xs" v-for="(colorItem,index) in color">		
		<div class="qui-flex-row-space-around">
		  <div v-for="(item, index) in 10" class="qui-flex1">
		    <div :class="[`bg-${colorItem}-${item}`,`qui-text`]">{{ `bg-${colorItem}-${item}` }}</div>
			<!-- {{ `bg-${colorItem}-${item}` }} -->
		  </div>
		</div>
	</div>
 
</template>

<style lang="scss">
// @import '../scss/index.scss';
@import "../scss/css/index.css";
.qui-divider-left {
  border-left-width: thick;
}
.qui-text{
	width: 100%;
	height: 10rpx;
}
</style>
