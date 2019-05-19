<template>
	<div class="big">
		<swiper v-if="imgUrls.length > 0" indicator-dots="true" autoplay="true" circular="true">
			<block v-for="(item, index) in imgUrls" :key="index">
				<swiper-item>
					<image class="banner" :src="item" mode="scaleToFill"></image>
				</swiper-item>
			</block>
		</swiper>
		<ul>
			<li v-for="content in books" :key="index">
					<navigator :url="content.book_url">
					<image class="book_image" :src="content.uurl"></image>
					<div class="li_content">
						<p class="li_name">{{content.name}}({{content.star}})</p>
						<p class="li_author">{{content.author}}</p><br />
						<p class="li_press">{{content.press}}</p>
					</div>
					<div class="li_right">
						<p>浏览量：{{content.look}}</p><br />
						<p>{{content.uploads}}</p>
					</div>
					</navigator>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				imgUrls: [
					"../../static/images/btt1.jpg",
					"../../static/images/btt2.jpg",
					"../../static/images/btt3.jpg"
				],
				books: [{
						name: "javaEE开发的颠覆者:springboot实战",
						author: "汪云飞",
						press: "电子工业出版社",
						star: 6.3,
						look: 3,
						uploads: "yangxd",
						uurl: "../../static/images/book1.jpg",
						book_url:"/pages/dianfuzhe/main"
					},

					{
						name: "程序员的数学3：线性代数",
						author: "[日]平冈和幸",
						press: "人民邮电出版社",
						star: 8.6,
						look: 4,
						uploads: "Codeer Or Gun",
						uurl: "../../static/images/book2.jpg",
						book_url:"/pages/cxymath/main"
					},

					{
						name: "微信小程序实战入门：内含完整实例解析",
						author: "刘明洋",
						press: "人民邮电出版社",
						star: 0,
						look: 3,
						uploads: "小小峰",
						uurl: "../../static/images/book3.jpg",
						book_url:"/pages/xcxszrm/main"
					},

					{
						name: "javaEE开发的颠覆者:springboot实战",
						author: "汪云飞",
						press: "电子工业出版社",
						star: 6.3,
						look: 3,
						uploads: "yangxd",
						uurl: "../../static/images/book1.jpg",
						book_url:"/pages/dianfuzhe/main"
					},

					{
						name: "程序员的数学3：线性代数",
						author: "[日]平冈和幸",
						press: "人民邮电出版社",
						star: 8.6,
						look: 4,
						uploads: "Codeer Or Gun",
						uurl: "../../static/images/book2.jpg",
						book_url:"/pages/cxymath/main"
					},

					{
						name: "微信小程序实战入门：内含完整实例解析",
						author: "刘明洋",
						press: "人民邮电出版社",
						star: 0,
						look: 3,
						uploads: "小小峰",
						uurl: "../../static/images/book3.jpg",
						book_url:"/pages/xcxszrm/main"
					}
				]
			}
		}
	}
</script>

<style>
	
	ul {
		margin-top: 20px;
	}
	
	body {
		font-size: 15px;
	}
	
	li {
		padding-bottom: 10px;
		border-bottom: 1px solid #dddddd;
		position: relative;
		display: block;
		width: 100%;
		float: left;
		margin-bottom: 20px;
	}
	
	.banner {
		width: 100%;
		height: 100%;
	}
	
	.book_image {
		float: left;
		width: 15%;
		height: 80px;
	}
	
	.li_name {
		display: inline;
	}
	
	.li_content p {
		display: block;
	}
	
	.li_content {
		float: left;
		overflow: hidden;
		display: inline-block;
		width: 60%;
	}
	
	.li_right {
		padding-right: 10px;
		position: absolute;
		right: 0;
		bottom: 10px;
		float: left;
	}
	
	.li_right p {
		float: right;
	}
</style>