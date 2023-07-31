<script>
	import NewsHeadline from './newsHeadline.svelte';
</script>

<main>
	<div class="new">
		<h1>New</h1>
		<NewsHeadline
			headline="Hydrogen VS Electric Cars"
			pragraph="Will hydrogen-fueled cars ever catch up to EVs?"
		/>
		<NewsHeadline
			headline="The Downsides of Al Artistry"
			pragraph=" What are the possible adverse effects of on-demand Al image generation?"
		/>
		<NewsHeadline
			headline="Is VC Funding Drying Up?"
			pragraph="Private funding by VC firms is down 50% YOY. We take a look at what that means."
		/>
	</div>
</main>

<style>
	main {
		width: 100vw;
		padding-inline: 1rem;
	}
	.new {
		width: 100%;

		padding: 1.5rem 1rem;
		background-color: var(--Very-dark-blue);
	}
	.new h1 {
		color: var(--Soft-orange);
		font-family: var(--ff-inter);
	}
	@media screen and (min-width: 1024px){
		main{
			width: 40vw;
	
		}
	}
</style>
