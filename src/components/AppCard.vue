<template>
		<div class="card d-flex flex-column my-card-container">
			<div>
				<img :src="image" :alt="title">
			</div>
			<div>
				<span class="text-white text-uppercase">{{ title }}</span>
			</div>
		</div>

</template>

<script>

	export default {
		name: 'AppCard',
		props: ['image', 'title'],
	}
</script>

<style lang="scss" scoped>
img{
	width: 100%;
	height: calc(100vh / 2);
}

</style>