<template>
	<view>
		<!-- tab导航开始 -->
			<view class="uni-tab-bar">
				<scroll-view scroll-x class="uni-swiper-tab">
					<block v-for="(item,index) in tabBars" :key="item.id">
						<view class="swiper-tab-list" :class="{'active':tabIndex==index}"
							@tap="tabtap(index)">
							{{item.name}}
							<view class="swiper-tab-line"></view>
						</view>
					</block>
				</scroll-view>
			</view>
			<view class="uni-tab-bar" >
				<swiper class="swiper-box" 
				:style="{height:swiperheight+'px'}"
				:current="tabIndex"
				@change="tabIndexchange">
					<swiper-item v-for="(items,index) in newslist" :key="index"> 
						<scroll-view scroll-y="true" class="list">
							<block v-for="(item,index1) in items.list" :key="index1">
								<index-list :item="item" :index="index1"></index-list>
							</block>
						</scroll-view>
					</swiper-item>
				</swiper>
			</view>
	</view>
</template>

<script>
	import indexList from "../../components/index/index-list.vue";
	export default {
		components:{
			indexList
		},
		data() {
			return {
				swiperheight:0,
				tabIndex:3,
				tabBars:[
					{name:"关注",id:"guanzhu"},
					{name:"推荐",id:"tuijian"},
					{name:"体育",id:"tiyu"},
					{name:"热点",id:"redian"},
					{name:"财经",id:"caijing"},
					{name:"娱乐",id:"yule"},
					{name:"高笑",id:"gaoxiao"},
				],
				newslist:[
					{
						list:[
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:true,
								title:'阮姐姐生活照',
								type:'img',//video:视频
								playnum:'',
								long:'',
								titlepic:'../../static/datapic/1.jpg',
								infonum:{//顶和踩
									index:2,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:1,
								},
								commentnum:"100w", //评论数
								sharenum:100,//分享数
								
							},
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:false,
								title:'阮姐姐在线打豆豆',
								type:'video',//video:视频，
								playnum:'20w',
								long:'2:47',
								titlepic:'../../static/datapic/10.jpg',
								infonum:{//顶和踩
									index:1,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:0,
								},
								commentnum:"100w", //评论数
								sharenum:10,//分享数
								
							}
						]
					},{
						list:[
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:true,
								title:'阮姐姐生活照',
								type:'img',//video:视频
								playnum:'',
								long:'',
								titlepic:'../../static/datapic/1.jpg',
								infonum:{//顶和踩
									index:2,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:1,
								},
								commentnum:"100w", //评论数
								sharenum:100,//分享数
								
							},
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:false,
								title:'阮姐姐在线打豆豆',
								type:'video',//video:视频，
								playnum:'20w',
								long:'2:47',
								titlepic:'../../static/datapic/10.jpg',
								infonum:{//顶和踩
									index:1,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:0,
								},
								commentnum:"100w", //评论数
								sharenum:10,//分享数
								
							}
						]
					},{
						list:[
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:true,
								title:'阮姐姐生活照',
								type:'img',//video:视频
								playnum:'',
								long:'',
								titlepic:'../../static/datapic/1.jpg',
								infonum:{//顶和踩
									index:2,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:1,
								},
								commentnum:"100w", //评论数
								sharenum:100,//分享数
								
							},
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:false,
								title:'阮姐姐在线打豆豆',
								type:'video',//video:视频，
								playnum:'20w',
								long:'2:47',
								titlepic:'../../static/datapic/10.jpg',
								infonum:{//顶和踩
									index:1,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:0,
								},
								commentnum:"100w", //评论数
								sharenum:10,//分享数
								
							}
						]
					},{
						list:[
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:true,
								title:'阮姐姐生活照',
								type:'img',//video:视频
								playnum:'',
								long:'',
								titlepic:'../../static/datapic/1.jpg',
								infonum:{//顶和踩
									index:2,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:1,
								},
								commentnum:"100w", //评论数
								sharenum:100,//分享数
								
							},
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:false,
								title:'阮姐姐在线打豆豆',
								type:'video',//video:视频，
								playnum:'20w',
								long:'2:47',
								titlepic:'../../static/datapic/10.jpg',
								infonum:{//顶和踩
									index:1,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:0,
								},
								commentnum:"100w", //评论数
								sharenum:10,//分享数
								
							}
						]
					},{
						list:[
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:true,
								title:'阮姐姐生活照',
								type:'img',//video:视频
								playnum:'',
								long:'',
								titlepic:'../../static/datapic/1.jpg',
								infonum:{//顶和踩
									index:2,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:1,
								},
								commentnum:"100w", //评论数
								sharenum:100,//分享数
								
							},
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:false,
								title:'阮姐姐在线打豆豆',
								type:'video',//video:视频，
								playnum:'20w',
								long:'2:47',
								titlepic:'../../static/datapic/10.jpg',
								infonum:{//顶和踩
									index:1,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:0,
								},
								commentnum:"100w", //评论数
								sharenum:10,//分享数
								
							}
						]
					},{
						list:[
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:true,
								title:'阮姐姐生活照',
								type:'img',//video:视频
								playnum:'',
								long:'',
								titlepic:'../../static/datapic/1.jpg',
								infonum:{//顶和踩
									index:2,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:1,
								},
								commentnum:"100w", //评论数
								sharenum:100,//分享数
								
							},
							{
								userpic:'../../static/userpic/4.jpg',
								username:'阮姐姐',
								isguanzhu:false,
								title:'阮姐姐在线打豆豆',
								type:'video',//video:视频，
								playnum:'20w',
								long:'2:47',
								titlepic:'../../static/datapic/10.jpg',
								infonum:{//顶和踩
									index:1,//0没有操作，1：顶     2：踩
									ding_num:1100,
									cai_num:0,
								},
								commentnum:"100w", //评论数
								sharenum:10,//分享数
								
							}
						]
					}
				],
				
			}
		},
		methods: {
			tabtap(index){
				console.log(index)
				this.tabIndex = index
			},tabIndexchange(e){
				console.log(JSON.stringify(e.detail.current))  //JSON对象转成字符串,获取滑动时的index
				this.tabIndex = e.detail.current;
				}
		},
		onLoad() {
			uni.getSystemInfo({
				success: (res) => {
					let height = res.windowHeight - uni.upx2px(80)
					console.log(height)
					this.swiperheight = height;
				}
			})
		}
	}
</script>
<style lang="scss">	
	
	
	.scroll-h {
	    width: 750rpx;
	    height: 80rpx;
	    flex-direction: row;
	    /* #ifndef APP-PLUS */
	    white-space: nowrap;
	    /* #endif */
		white-space: nowrap;
	    /* flex-wrap: nowrap; */
	    border-color: #cccccc;
		white-space: nowrap;
		border-bottom-style: solid;
		border-bottom-width: 1px;
	}
	
	
	.uni-tab-item {
	    /* #ifndef APP-PLUS */
	    display: inline-block;
	    /* #endif */
		display: inline-block;
	    flex-wrap: nowrap;
	    padding-left: 34rpx;
	    padding-right: 34rpx;
		font-size: 30rpx;
	}
	.active {
	    color: #000;
		font-weight: bold;
	}
	.active .swiper-tab-line{
		border-bottom: 4upx solid #FEDE33;
		width: 60upx;
		margin: auto;
		border-top:4upx solid #FFE933;
		border-radius:20upx ;
	}
	.swiper-box {
	    flex: 1;
	
	}

</style>
