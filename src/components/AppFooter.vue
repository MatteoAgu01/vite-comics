<template>
	<footer class="w-100">
		<!-- market place  -->
		<div class="bg-primary my-z">
			<div class="my-market d-flex align-items-center justify-content-center ">
				<ul class="d-flex justify-content-center  m-0">
					<li v-for="(bar, index) in MarketPlace" :key="index" class="d-flex align-item-center flex-column flex-md-row text-sm-center">
						<div class="px-3 d-flex align-self-center">
							<img :src="bar.img" :alt="bar.text">
						</div>
						<div class="text-white d-flex align-self-center">
							<p class="m-0">
								{{ bar.text }}
							</p>
						</div>
					</li>
				</ul>
			</div>
		</div>
		<!--// market place  -->

		<!-- main footer -->
			<div class="my-body-footer d-flex  justify-content-md-center justify-content-md-around px-sm-5">
				<ul class="d-flex flex-column flex-wrap gap-1 m-0">
					<li v-for="(footers, index) in ulFooter" :key="index" class="mx-4">
						<h3 class="text-white p-0 my-3">{{ footers.title }}</h3>
						<ul class="p-0">
							<li v-for="(child, index2) in footers.list" :key="index2">
								<p class="text-secondary m-0 p-0">{{ child }}</p>
							</li>
						</ul>
					</li>
				</ul>
			
					<img class="my-relative" src="../../public/img/dc-logo-bg.png" alt="">
			
			</div>
		<!-- //main footer -->

		<!-- social and sing in -->
		<div class="bg-dark p-4 social-footer">
			<div class="d-flex justify-content-between align-items-center w-75 m-auto" >
				<div class="d-flex align-items-center">
					<button class="text-uppercase border border-primary bg-dark text-white p-2">
						sing-up now
					</button>
				</div>
				<div class="d-flex align-items-center">
					<h4 class="text-uppercase text-primary">
						follow us
					</h4>
					<img class="px-3  d-none d-md-block" src="../../public/img/footer-facebook.png" alt="facebook">
					<img class="px-1 d-none d-md-block" src="../../public/img/footer-twitter.png" alt="twitter">
					<img class="px-1 d-none d-md-block" src="../../public/img/footer-youtube.png" alt="youtube">
					<img class="px-1 d-none d-md-block" src="../../public/img/footer-pinterest.png" alt="pintrest">
					<img class="px-1 d-none d-md-blomd" src="../../public/img/footer-periscope.png" alt="periscope">
				</div>
			</div>
		</div>
		<!-- //social and sing in -->

	</footer>
</template>

<script>
import { footers } from '../data/data.js';
import { bar } from '../data/data.js';
export default {
	name: 'AppFooter',
	data() {
		return {
			MarketPlace: bar,
			ulFooter: footers
		}
	},
}
</script>

<style lang="scss" scoped>
.my-market {
	width: 100%;
	min-height: 80px;
	height: 15vh;
	position: relative;
	z-index: 20;
}
.my-market img{
	width: 50px;
}

.my-market li{
	width: calc(100% / 2);
}
.my-market ul{
	width: calc(100% / 2);
}

ul{
	list-style-type: none;
	max-height: 40vh;
}

.my-body-footer{
	background-image: url(../../public/img/footer-bg.jpg);
	background-position: center;
	background-size: cover;
	position: relative;
}

.social-footer{
	height: 100px;
	width: 100%;
	position: fixed;
	bottom: 0;
	z-index: 2;
}

.my-relative{
	position: relative;
	bottom: 45px;
	z-index: 1;
}

.my-z{
	position: relative;
	z-index: 2;
}

@media screen and (max-width:768px){
	.my-market img{
		width: 40px;
		margin: 10px;
	}

	.my-market{
		height: 25vh;
	}

	.my-relative{
		scale: 30%;
		bottom: 80px;
	}
}
@media screen and (max-width:768px){
	.my-relative{
		display: none;
	}
	.my-body-footer{
		font-size: 0.4rem;
		margin-bottom: 99px;
		padding-bottom: 10px;
}
}
</style>