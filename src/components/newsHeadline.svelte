<script>
	export let pragraph;
	export let headline;
</script>

<div class="newsHeadline">
	<h1>{headline}</h1>
	<p>{pragraph}</p>
</div>

<style>
	.newsHeadline {
		border-bottom: 2px var(--Grayish-blue) solid;
		padding-block: 1.5rem;
		font-family: var(--ff-inter);
		color: var(--Off-white);
	}
	h1 {
		font-size: 1.5rem;
	}
	p {
		color: var(--Grayish-blue);
		line-height: 2;
	}
</style>
