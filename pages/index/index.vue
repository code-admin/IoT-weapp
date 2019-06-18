<template>
	<view class="content">
		<view>
			<van-search :value="value" placeholder="请输入搜索关键词" @search="onSearch"></van-search>
			<view class="uni-padding-wrap">
				<view class="page-section swiper">
					<view class="page-section-spacing">
						<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
							<swiper-item>
								<view class="swiper-item uni-bg-red">智能井盖</view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item uni-bg-green">电力电表</view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item uni-bg-blue">智慧烟感</view>
							</swiper-item>
						</swiper>
					</view>
				</view>
			</view>
		</view>
		<image class="logo" src="/static/imgs/qt_logo_200.png"></image>
		<view>
			<text class="title">{{title}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '契通天地，万物互联',
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500,
			}
		},
		onLoad() {

		},
		methods: {
			onSearch() {
				console.log('onSearch');
			},
			onCancel() {
				console.log('onCancel');
			}
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
