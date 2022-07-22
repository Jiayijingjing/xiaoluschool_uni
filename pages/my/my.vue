<template>
	<view class="content">
		{{selected}}
		<Mytabbar :selected="selected"></Mytabbar>
	</view>
</template>

<script>
	import Mytabbar from '../../custom-tab-bar/index.vue'
	export default {
		data() {
			return {
				selected:4
			};
		},
		components:{
			Mytabbar
		}
	}
</script>

<style lang="scss">

</style>
