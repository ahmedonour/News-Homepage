<script>
	import Cards from '../components/Cards.svelte';
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
	<div class="flexSection">
		<Cards src="/images/image-retro-pcs.jpg" num="01" h_one="Reviving Retro PCs" parghraph="What happens when old PCs are given modern upgrades?"/>
		<Cards src="/images/image-top-laptops.jpg" num="02" h_one="Top 10 Laptops of 2022" parghraph="Our best picks for various needs and budgets."/>
		<Cards src="/images/image-gaming-growth.jpg" num="03" h_one="Top 10 Laptops of 2022" parghraph="Our best picks for various needs and budgets."/>
	</div>
</main>
<style>
	.flexSection{
		width: 100vw;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		padding-inline: 1rem;
		padding-block: 2rem;
	}
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
		.flexSection{
			width: 80vw;
			flex-direction: row;
			height: 50vh;
		}
	}
</style>
