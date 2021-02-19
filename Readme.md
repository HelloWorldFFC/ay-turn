
## 前言
简介：
1.翻转效果组件：
	有4个类型：1:3d  2:翻页 3：自动翻页 4： 2d平面
2.自定义主题色，和显示内容等，开箱即用

## 有疑问
微信搜索“慢慢向好”小程序，找客服反馈，相应问题。
				  

## 素材
[图片资源](https://pixabay.com)

## 示例项目可直接运行 
## 开始使用
下载源码解压，复制`/components` 下的组件至项目根目录的 `/components` 文件夹下

`index.vue`的`script`加入如下部分（自行选择需要展示的部分）：
```
import ayturn from '@/components/ay-turn/ay-turn.vue';
	export default {
		components: {
			ayturn,
		},

		data() {
			return {
				list: [{

					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{

					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},
				{
					img: 'https://cdn.pixabay.com/photo/2021/02/01/18/50/drop-5971598__340.jpg',
				},],
				list_page:[{
					size: '',
					img: 'https://cdn.pixabay.com/photo/2021/01/25/11/54/woman-5948133__340.jpg',
					txt: '名人名言',
				},
				{
					size: 1,
					txt: '开口就讲困难，成长已经远离你；一付出就想回报，机会已经远离你；一做事就在想个人利益，收获已经远',
				},
				{
					size: 2,
					txt: '离你；一有起色就在想谈条件，未来已经远离你；一合作就想自己如何不吃亏，事业已经远离你……格局有',
				},
				{
					size: 3,
					txt: '多大成就有多大！选择了安逸舒适，就不必羡慕别人的精彩；选择了惊涛骇浪，就无须向往岁月静好。不同',
				},
				{
					size: 4,
					txt: '的选择给予你不同的生活路径。只要认定你内心真正想要的，并为之持续努力，每个人都会是自己的人生赢家！',
				},
				{
					size: 5,
					txt: '但凡成功之人，往往都要经历一段没人支持、没人帮助的黑暗岁月，而这段时光，恰恰是沉淀自我的关键阶',
				},
				{
					size: 6,
					txt: '段。犹如黎明前的黑暗，捱过去，天也就亮了。所谓千里马，不一定是跑得最快的，但一定是耐力最好的。',
				},
				{
					size: 7,
					txt: '可以抱怨，但必须忍耐，积蓄力量，等待机会——这样，人生才会有希望。生命是一场从蒙昧到清醒的追寻。',
				},
				{
					size: 8,
					txt: '若能时时刻刻保持察觉，我们将可以在痛苦中找到恩典，可以少一些怀疑，多一些相信。生活越是艰苦，人就越',
				},
				{
					size: 9,
					txt: '发坚强；人越是坚强，生活也就变得越发简单。',
				},],
				list_page_auto:[{
					size: 5,
					txt: '修身治国平天下555',
				},
				{
					size: 4,
					txt: '修身治国平天下44444444',
				},
				{
					size: 3,
					txt: '修身治国平天下3333',
				},
				{
					size: 2,
					txt: '修身治国平天下222222222',
				},
				{
					size: 1,
					txt: '修身治国平天下11111',
				},],
				cover_auto:{},
		
				pros_img:'https://cdn.pixabay.com/photo/2020/03/13/08/34/south-station-4927286__340.jpg',
				cons_img:'https://cdn.pixabay.com/photo/2021/01/11/18/41/snowfall-5909261__340.jpg',
			}
		},
		onLoad() {
			let that = this;
			that.loadData();
		},
		onShow() {

		},
		// #ifdef MP-WEIXIN
		//微信小程序的分享
		onShareAppMessage: function(options) {
		
		},
		// #endif
		methods: {
			async loadData() {
				let that = this;
			
				
				
			},
		}
	}

```


`index.vue`的`template`加入如下部分：
```
<view>
		
		<view style="margin-top: 130upx;">
			<!-- 3d的会影响闪动一下，但不影响单独使用 -->
			<ayturn :type="3" :height="400" :width="300" :cover="cover_auto"  :list="list_page_auto"></ayturn>
		</view>
		
		
		
		<ayturn :type="1" :height="100" :width="200"  :list="list"></ayturn>
		
		<ayturn :type="4"  :height="150" :width="150" :pros_img="pros_img" :cons_img="cons_img"></ayturn>
		
		<ayturn :type="2" :height="640" :width="400" :list="list_page"></ayturn>
		
		<ayturn :type="1" :height="100" :width="200"  :list="list"></ayturn>
		<ayturn :type="1":height="100" :width="200" :marginTop="10" :list="list"></ayturn>
		<ayturn :type="1" :height="100" :width="200" :marginTop="10" :list="list"></ayturn>
		<ayturn :type="1" :height="100" :width="200" :marginTop="10" :list="list"></ayturn>
		<ayturn :type="1" :height="100" :width="200" :marginTop="10" :list="list"></ayturn>
		<ayturn :type="1" :height="100" :width="200" :marginTop="10" :list="list"></ayturn>
		<ayturn :type="1" :height="100" :width="200" :marginTop="10" :list="list"></ayturn>
	</view>
```
 

## 参考
[参考链接1](https://www.cnblogs.com/zyrblog/p/11142624.html)
[参考链接2](https://www.jianshu.com/p/f2b324c1081d)
[参考链接3](https://github.com/heavenYJJ/css3/blob/master/translate-book.html)
[参考链接4](https://ext.dcloud.net.cn/plugin?id=3685)

供学习整理，易于下次便捷使用与快捷重复使用，如有任何冒犯的地方，可微信搜索“慢慢向好”小程序，找客服说明删除