<template>
	<view>
		<!-- 首页的文章开始 -->
		<view class="index-list">
			<view class="index-list1">
				<view>
					<image src="../../static/userpic/4.jpg" mode="widthFix" lazy-load></image>
					昵称
				</view>
				<view>
					<view class="iconfont icon-zengjia"></view>关注
				</view>
			</view>
			<view class="index-list2">我是标题</view>
			<view class="index-list3">
				<image src="../../static/datapic/1.jpg" mode="widthFix"></image>
			</view>
			<view class="index-list4">
				<view>
					<view><view class="iconfont icon-icon_xiaolian-mian"></view>10</view>
					<view><view class="iconfont icon-kulian"></view>10</view>
				</view>
				<view>
					<view><view class="iconfont icon-pinglun1"></view>10</view>
					<view><view class="iconfont icon-zhuanfa"></view>10</view>
				</view>
			</view>
		</view>
		<view class="index-list">
			<view class="index-list1">
				<view>
					<image src="../../static/userpic/4.jpg" mode="widthFix" lazy-load></image>
					昵称
				</view>
				<view>
					<view class="iconfont icon-zengjia"></view>关注
				</view>
			</view>
			<view class="index-list2">我是标题</view>
			<view class="index-list3">
				<!-- 图片 -->
				<image src="../../static/datapic/1.jpg" mode="widthFix"></image>
				<!-- 视频 -->
				<view class="iconfont icon-bofang index-list-play"></view>
				<view class="index-list-playinfo">
						20w次播放 2：47
				</view>
			</view>
			<view class="index-list4">
				<view>
					<view><view class="iconfont icon-icon_xiaolian-mian"></view>10</view>
					<view><view class="iconfont icon-kulian"></view>10</view>
				</view>
				<view>
					<view><view class="iconfont icon-pinglun1"></view>10</view>
					<view><view class="iconfont icon-zhuanfa"></view>10</view>
				</view>
			</view>
		</view>
		<!-- 首页的文章结束 -->
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {

		}
	}
</script>
<style lang="scss">	
	.index-list{
		padding: 20px;
		border-bottom: 1px solid #CCCCCC;
		font-size: 14px;
	}
	.index-list1{
		@include flexs();
	}
	.index-list1>view:first-child{
		display: flex;
		align-items: center;
		color: #999999;
		
	}
	.index-list1>view:first-child image{
		width: 90upx;
		height: 90upx;
		border-radius: 50%;
		margin-right: 15upx;
	}
	.index-list1>view:last-child{
		@include flexs();
	}
	.index-list1>view:last-child{
		background-color: #F4F4F4;
		border-radius: 5upx;
		padding:5upx 10upx;
	}
	.index-list2{
		// color: ;
		padding: 25upx 0;
		font-size: 32upx;
	}
	.index-list3{
		position: relative;
		padding-top: 15upx;
align-items: center;
	
	}
	.index-list3>image{
		width: 100%;
		border-radius: 20upx;
		
	}
	.index-list4{
		padding-top:25upx ;
		@include flexs();
	}
	.index-list4 view{
		color: #999999;
	}
	.index-list4>view:first-child{
		@include flexs();
	}
	.index-list4>view:first-child view{
		@include flexs();
	}
	.index-list4>view:last-child{
		@include flexs();
	}
	.index-list4>view:last-child view{
		@include flexs();
	}
	.index-list4>view>view>view{
		margin-right: 5;
	}

	.index-list4>view:first-child>view{
		margin-right: 10upx;
	}
	.index-list4>view:last-child>view{
		margin-left: 10upx;
	}
	// 视频样式开始
	.index-list-play{
		position: absolute;
	}
	.index-list-playinfo{
		position: absolute;
	}
	// 视频样式结束
</style>
