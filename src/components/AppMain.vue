<template>
	<main class=" bg-dark w-100 px-5">
		<div>
			<div class="col-12  w-100 d-flex flex-wrap justify-content-center ">
				<AppCard :image="copertine.thumb" :title="copertine.series" v-for="(copertine, index) in cardPreview"
					:key="index" />
			</div>
		</div>
	</main>
</template>

<script>
import { copertine } from '../data/dc-comics';
import AppCard from './AppCard.vue';
export default {
	name: 'AppMain',
	data() {
		return {
			cardPreview: copertine
		}
	},
	components: {
		AppCard
	}

}
</script>

<style lang="scss" scoped>
main {
 padding: 5%;
}
.my-card-container{
	width: calc(100vh / 2.5);
	margin: 4px;
	padding: 3px;
	background-color: rgb(27, 27, 27);
}
</style>