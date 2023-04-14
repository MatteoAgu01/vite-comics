<template>
	<header class="w-100">
		<!-- MAIN NAV BAR -->
		<div class="w-75 d-flex align-items-center px-5 py-3 m-auto">
			<!-- logo -->
			<div class="w-25">
				<img   src="../../public/img/dc-logo.png" alt="logoDc">
			</div>
			<!-- //logo -->

			<!-- nav bar link -->
			<div class="w-75">
				<ul class="d-md-flex flex-wrap justify-content-center m-0 d-none" >
					<li class="d-flex flex-column align-items-center gap-5 mx-2 my-li-link " v-for = "( header, index ) in navLink" :key="index">
						<div class="d-flex align-items-start justify-content-center justify-self-start my-text-blue">
							<a class="my-text-blue fw-bold" href=" header.url ">{{ header.text }}</a>
						</div>
						<div class="d-flex justify-self-end my-bg-blue">

						</div>
					</li>
				</ul>
			</div>
			<!--// nav bar link -->
		</div>
		<!-- //MAIN NAV BAR -->
	</header>
</template>

<script>
import { header } from '../data/data.js';
	export default {
		name: 'headerComponents',
		data(){
			return{
				navLink: header
			};
		}
	}

</script>

<style lang="scss" scoped>
.my-bg-blue{
	opacity: 0;
	background-color: rgb(53, 53, 253);
	height: 5px;
	width: 80%;
	cursor: pointer;
	transition: 0.4s;
}

.my-text-blue{
	color: black;
	text-transform: uppercase;
	text-decoration: none;
	transition: 0.4;
}

.my-li-link:hover .my-bg-blue{
	opacity: 1;

}

.my-li-link:hover .my-text-blue{
	color: rgb(53, 53, 253);
}

.my-li-link{
	cursor: pointer;
}
</style>