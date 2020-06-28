<template>
	<view class="index-list">
		<view class="index-list1">
			<view>
				<image :src="item.userpic" mode="widthFix" lazy-load></image>
				{{item.username}}
			</view>
			<view  v-show="!item.isguanzhu">
				<view class="iconfont icon-zengjia"></view>关注
			</view>
		</view>
		<view class="index-list2">{{item.title}}</view>
		<view class="index-list3">
			<!-- 图片 -->
			<image :src="item.titlepic" mode="widthFix" lazy-load></image>
			<!-- 视频 -->
			<template v-if="item.type == 'video'">
				<view class="iconfont icon-bofang index-list-play"></view>
				<view class="index-list-playinfo">
						{{item.playnum}}次播放{{item.long}}
				</view>
			</template>
		</view>
		<view class="index-list4">
			<view>
				<view :class="{'active':(item.infonum.index == 1)}"><view class="iconfont icon-icon_xiaolian-mian"></view>{{item.infonum.ding_num}}</view>
				<view :class="{'active':(item.infonum.index == 2)}"><view class="iconfont icon-kulian"></view>{{item.infonum.cai_num}}</view>
			</view>
			<view>
				<view><view class="iconfont icon-pinglun1"></view>{{item.commentnum}}</view>
				<view><view class="iconfont icon-zhuanfa"></view>{{item.sharenum}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			item:Object,
			index:Number,
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
	}
	.index-list3>image{
		width: 100%;
		border-radius: 20upx;
		
	}
	// 视频样式开始
	.index-list-play{
		position: absolute;
		font-size: 100upx;
		color: #FFFFFF;
		top: 35%;
		left: 42%;
		
	}
	.index-list-playinfo{
		position: absolute;
		font-size: 22upx;
		padding: 10upx 18upx;
		border-radius: 40upx;
		color: #FFFFFF;
		background-color: rgba(51,51,51,0.72);
		bottom: 20upx;
		right: 20upx;
	}
	// 视频样式结束
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
	.index-list4 .active ,.index-list4 .active>view{
		color: #C5F61C;
	}
</style>
