<main>
	<img src="/images/image-web-3-desktop.jpg" alt="" id="desktop"/>
	<img src="/images/image-web-3-mobile.jpg" alt="" id="mobile"/>

	<h1>The Bright Future of Web 3.0?</h1>
	<p>
		We dive into the next evolution of the web that claims to put the power of the platforms back
		into the hands of the people But is it really fuifiting its promise?
	</p>
	<button>Read More</button>
</main>

<style>
	main {
		width: 100vw;
		padding-inline: 1rem;
		margin-bottom: 2rem;
	}
	#desktop{
		display: none;
	}
	img {
		width: 100%;
	}
	h1 {
		font-family: var(--ff-inter);
		font-size: 2.5rem;
		color: var(--Very-dark-blue);
	}
	p {
		font-family: var(--ff-inter);
		line-height: 2;
		color: var(--Grayish-blue);
		font-size: 1rem;
		font-weight: 400;
	}
	button {
		width: 200px;
		height: 40px;
		border: none;
		font-family: var(--ff-inter);
		text-transform: uppercase;
		letter-spacing: 2px;
		font-weight: 700;
		margin-top: 1rem;
		color: var(--Off-white);
		background-color: var(--Soft-red);
	}
	@media screen and (min-width: 1024px){
		#mobile{
			display: none;
		}
		#desktop{
			display: block;
		}
		main{
			width: 80vw;
			display: grid;
			grid-template-columns: repeat(2,1fr);
			grid-template-rows: repeat(3,1fr);
			gap: 2rem;

		}
		img{
			grid-column: 1 / span 2;
			grid-row: 1;
		}
		h1{
			font-size: 4rem;
			grid-column: 1;
			grid-row: 2 / span 3;
		}
		p{
			font-size: 1.2rem;
			grid-column: 2;
			grid-row: 2/3;
		}
		button{
			grid-column: 2;
			grid-row: 3;
		}
	}
</style>
