<template>
	<view class="content">
		<button type="primary" @tap="doss">点击签名1</button>
		<button type="primary" @tap="doss2">点击签名2</button>
		
		<view class="imgs">
			<image class="img" :src="img1" mode="widthFix"></image>
			<image class="img" :src="img2" mode="widthFix"></image>
		</view>
		
		<catSignature canvasId="canvas1"  @close="close" @save="save" :visible="isShow" />
		<catSignature canvasId="canvas2" @close="close2" @save="save2" :visible="isShow2" />
		
		
	</view>
</template>

<script>
	import catSignature from "@/components/cat-signature/cat-signature.vue"
	export default {
		components:{catSignature},
		data() {
			return {
				img1:'',
				img2:'',
				isShow:false,
				isShow2:false,
			}
		},
		onLoad() {

		},
		methods: {
			doss(){
				this.isShow = true;
			},
			close(){
				this.isShow = false;
			},
			save(val){
				this.isShow = false;
				this.img1 = val
			},
			doss2(){
				this.isShow2 = true;
			},
			close2(){
				this.isShow2 = false;
			},
			save2(val){
				this.isShow2 = false;
				this.img2 = val
			},
		}
	}
</script>

<style>
	.imgs{width: 500upx;height: 500upx;display: flex;margin: 0 auto;flex-wrap: wrap;}
	.imgs img{width: 100%; height: 100%;}
</style>
