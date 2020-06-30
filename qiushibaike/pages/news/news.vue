<template>
	<view class="index">
		<!-- 自定义导航栏-->
		<uni-nav-bar :statusBar="true" @clickRight="openAdd">
			<!-- 左边 -->
			<block slot="left">
				<view class="nav-left">
					<view class="iconfont icon-qiandao"></view>
				</view>
			</block>
			<!-- 中间 -->
			<view class="nav-tab-bar u-f-ajc">
				<block v-for="(tab,index) in tabBars" :key="tab.id">
					<view class="active" :class="{'active':tabIndex==index}" @tap="changeTab(index)">
						{{tab.name}}
						<view v-if="(tabIndex==index)" class="nav-tab-bar-line"></view>
					</view>
					
				</block>
			</view>
			<!-- 右边 -->			
			<block slot="right">
				<view class="nav-right u-f-ajc">
					<view class="iconfont icon-bianji1"></view>
				</view>
			</block>
		</uni-nav-bar>
		<!-- 列表开始 -->
		<view class="common-list">
			<!-- 左边头像开始 -->
			<view class="common-list-l">
				<image src="../../static/userpic/12.jpg" mode="widthFix"></image>
			</view>
			<!-- 左边头像结束 -->
			<!-- 右边内容开始 -->
			<view class="common-list-r">
				<view class="u-f-ac u-f-jsb">
					<view class="u-f">
						昵称
						<view class="tag-sex iconfont icon-nan">
							25
						</view>
					</view>
					<view class="iconfont icon-zengjia">
						关注
					</view>
				</view>
				<view>我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题我是标题</view>
				<view class="u-f-ajc">
					<!-- 图片 -->
					<image 
					src="../../static/datapic/13.jpg" 
					mode="widthFix" 
					lazy-load></image>
					<!-- 视频 -->
					<view class="common-list-play iconfont icon-bofang"></view>
					<view class="common-list-playinfo">
						20w 次播放
					</view>
				</view>
				<view class="u-f-ac u-f-jsb">
					<!-- 左边 -->
					<view class="">
						深圳 龙岗
					</view>
					<!-- 右边 -->
					<view class="u-f-ac">
						<view class="iconfont icon-zhuanfa">10</view>
						<view class="iconfont icon-xiaoxi">10</view>
						<view class="iconfont icon-fenxiang">20</view>
					</view>
				</view>
			</view>
			<!-- 右边内容结束 -->
		</view>
		<!-- 列表结束 -->
	</view>
</template>

<script>
	import uniNavBar from '../../components/uni-nav-bar/uni-nav-bar.vue'
	export default {
		components:{
			uniNavBar
		},
		data() {
			return {
				tabIndex:0,
				tabBars:[
					{name:"关注",id:"guanzhu"},
					{name:"话题",id:"topic"}
				]
			}
		},
		methods: {
			changeTab(index){
				this.tabIndex = index;
			},
			openAdd(){
				console.log(123)
				uni.navigateTo({
					url:'../add-input/add-input',
				});
			}
		}
	}
</script>

<style lang="scss">

.nav-left>view,.nav-right>view{
	font-size:45upx;
}
.nav-left>view{
	color: #FF9619;
}
.nav-left{
	margin-left: 16upx;
}
.nav-right{
	width: 100%;
}
.nav-tab-bar{
	width: 100%;
	position: relative;
	margin-left: -17upx;
}
.nav-tab-bar>view{
	font-size: 32upx;
	padding: 0 15upx;
	font-weight: bold;
	color: #969696;
}
.active{
	color: #333333;
	display: flex;
	/* align-items: center; */
	justify-content: center;
}
.active .nav-tab-bar-line{
	position: absolute;
	bottom: 0;
	border-bottom: 4upx solid red;
	border-top: 4upx solid red;
	width: 65upx;
	border-radius: 20upx;
}
//列表
.common-list{
	padding: 20upx;
	display: flex;
}

.common-list-l>image{
	width: 90upx;
	height: 90upx;
	border-radius: 100%;
}
.common-list-r{
	width: 90%;
	flex: 1;
	margin-left: 10upx;
	padding-bottom: 10upx;
	border-bottom: 1upx solid #EEEEEE;
}
.common-list-r>view:nth-child(1)>view:first-child{
	color: #999999;
	font-size: 30upx;
}
.common-list-r>view:nth-child(1)>view:last-child{
	background-color: #EEEEEE;
	padding: 0 20upx;
	font-size: 26upx;
}
.tag-sex{
	background-color: #007AFF;
	color: #FFFFFF;
	font-size: 23upx;
	padding: 0upx 17upx;
	margin-left:10upx ;
	border-radius: 20upx;
	line-height: 27px;
}
.common-list-r>view:nth-child(2){
	font-size: 32upx;
	padding: 12upx 0;
	margin-bottom: 3upx;
	
}
.common-list-r>view:nth-child(3){
	position: relative;
	margin-bottom: 20upx;
}
.common-list-play,.common-list-playinfo{
	position: absolute;
}
.common-list-play{
	font-size: 150upx;
	color: #FFFFFF;
}
.common-list-playinfo{
	right: 10upx;
	bottom: 10upx;
	background-color:rgba(51,51,51,0.73);
	color: #fff;
	border-radius: 20upx;
	padding: 0 15upx;
}
.common-list-r>view:nth-child(4){
	color: #AAAAAA;
}
.common-list-r>view:nth-child(4)>view:nth-child(2)>view{
	margin-left: 20upx;
	padding-left: 8upx;
}
.common-list-r>view:nth-child(3){
	width: 100%;
}
.common-list-r>view:nth-child(3)>image{
	width: 100%;
	border-radius: 10upx;
}
</style>
