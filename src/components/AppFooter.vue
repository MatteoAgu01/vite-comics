<template>
	<footer class="w-100">
		<!-- market place  -->
		<div class="bg-primary">
			<div class="my-market d-flex align-items-center justify-content-center">
				<ul class="d-flex justify-content-center  m-0">
					<li v-for="(bar, index) in MarketPlace" :key="index" class="d-flex align-item-center">
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

			<div>
				<ul>
					<li v-for="(footers, index) in ulFooter" :key="index">
						<h3>{{ footers.title }}</h3>
						<ul>
							<li v-for="(child, index2) in footers.list" :key="index2">
								<p>{{ child }}</p>
							</li>
						</ul>
					</li>
				</ul>
			</div>


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
	height: 20vh;
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
</style>