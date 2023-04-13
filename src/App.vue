<template>
	<AppHeader/>
	<AppMain/>
	<AppFooter/>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
	export default {
		name: 'App',
		components: {
			AppHeader,
			AppMain,
			AppFooter
		}
	}
</script>

<style lang="scss" scoped>

</style>
