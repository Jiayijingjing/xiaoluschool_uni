<template>
	<view class="classes" @tap="godatail">
		<itemclass v-for="(item,index) in list" :key="index" :urls="item"></itemclass>
	</view>
</template>

<script>
	import itemclass from '../itemclass/itemclass.vue'
	export default {
		data() {
			return {
				list:['../../static/itemsthree.png','../../static/itemsfour.png','../../static/items.png','../../static/itemone.png','../../static/itemsfour.png','../../static/itemsthree.png','../../static/itemstwo.png','../../static/items.png','../../static/itemsfour.png','../../static/itemsthree.png','../../static/itemstwo.png','../../static/items.png']
			};
		},
		components:{
			itemclass
		},
		methods:{
			godatail(){
				uni.navigateTo({
					url:'../classdatail/classdatail'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>

</style>
