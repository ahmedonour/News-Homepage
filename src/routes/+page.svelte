<script>
	import HeroSection from '../components/HeroSection.svelte';
	import NewSection from '../components/NewSection.svelte';
	import Nav from '../components/nav.svelte';
</script>

<main>
	<Nav />
	<div class="gridSection">
		<HeroSection />
		<NewSection />
	</div>
</main>
<style>
	@media screen and (min-width: 1024px){
		main{
			display: grid;
			place-items: center;
			grid-template-columns: 3;
			grid-template-rows: 2;

		}
		.gridSection{
			display: flex;
			width: 80vw;
			height: 90vh;
		}
	}
</style>
