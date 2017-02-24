<template>
    <div class="container">
		<app-header></app-header>
        <hr>
		<app-center></app-center>
        <hr>
        <app-footer></app-footer>
    </div>
</template>

<script>

	import Header from './Header.vue';
	import Footer from './Footer.vue';
	import Center from './Center.vue';

	export default {
		components: {
			'app-header': Header,
			'app-footer': Footer,
			'app-center': Center
		}
	}

</script>

<style>

</style>
