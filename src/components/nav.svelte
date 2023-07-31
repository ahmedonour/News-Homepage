<script>
	import { fade, fly } from 'svelte/transition';
	var visible = false;
	function toggleVisible() {
		visible = !visible;
	}
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/f3c7bd6f07.js" crossorigin="anonymous"></script>
</svelte:head>
<main>
	<nav>
		<h1><a href="/"><img src="/images/logo.svg" alt="" srcset="" id="logo" /></a></h1>
		<button on:click={toggleVisible}>
			<svg viewBox="0 0 100 80" width="40" height="40">
				<rect width="100" height="10" rx="10" />
				<rect y="30" width="100" height="10" rx="10" />
				<rect y="60" width="100" height="10" rx="10" />
			</svg>
		</button>
		<div
			class="bg"
			class:open={visible}
			in:fly={{ y: 100, duration: 500 }}
			out:fly={{ x: -100, duration: 500 }}
		>
			<ul>
				<button on:click={toggleVisible}
					><img src="/images/icon-menu-close.svg" alt="" srcset="" id="menu-close" /></button
				>

				<!-- svelte-ignore a11y-click-events-have-key-events -->
				<li on:click={() => (visible = false)}><a href="/" class:open={visible}>Home</a></li>
				<!-- svelte-ignore a11y-click-events-have-key-events -->
				<li on:click={() => (visible = false)}><a href="/about" class:open={visible}>New</a></li>
				<!-- svelte-ignore a11y-click-events-have-key-events -->
				<li on:click={() => (visible = false)}><a href="/work" class:open={visible}>Popular</a></li>
				<li on:click={() => (visible = false)}>
					<a href="/work" class:open={visible}>Trending</a>
				</li>
				<li on:click={() => (visible = false)}>
					<a href="/work" class:open={visible}>Categories</a>
				</li>
			</ul>
		</div>
	</nav>
</main>

<style>
	:global(body.dark-mode) {
		--clr-Black: #e4d79d;
		--clr-SkyBlue: #132f4d;
		--clr-Blue: #e61e33;
		--clr-NavBG: rgba(0, 0, 0, 0.219);
	}

	.fas {
		cursor: pointer;
	}
	main {
		width: var(--width-Scroll);
		display: grid;
		place-items: center;
	}
	nav {
		display: flex;
		width: 100vw;
		padding: 1rem;
		height: 100px;
		justify-content: space-between;
		align-items: center;
	}
	#logo {
		width: 40px;
	}
	#menu-close {
		position: absolute;
		top: 20px;
		right: 20px;
	}
	nav a {
		text-decoration: none;
		color: var(--clr-Black);
	}
	nav h1 {
		font-family: var(--ff-sec);
		font-size: 2.5rem;
	}
	.bg {
		display: none;
	}
	.bg.open {
		display: flex;
		width: 100vw;
		height: 100vh;
		position: absolute;
		top: 0;
		left: 0;
		background-color: rgba(0, 0, 0, 0.201);
	}
	nav .bg ul {
		display: none;
	}
	nav .bg ul {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		padding-left: 1.5rem;
		width: 65vw;
		height: 100vh;
		position: absolute;
		top: 0px;
		right: 0;
		list-style: none;
		background-color: var(--Off-white);
		font-size: 1.5rem;
		font-family: var(--ff-inter);
		backdrop-filter: blur(10px);
		-webkit-backdrop-filter: blur(10px);
		z-index: 99999;
	}
	nav .bg ul li {
		font-weight: 400;
		margin-bottom: 2rem;
	}
	nav .bg ul li::marker {
		color: var(--clr-Blue);
	}
	nav button {
		background: none;
		border: none;
		font-size: 2rem;
	}

	@media screen and (min-width: 1024px) {
		#logo {
		width: 80px;
	}
		nav {
			width: 80vw;
			height: 150px;
			justify-content: space-between;
		}
		nav button {
			display: none;
		}
		.bg {
			display: flex;
			width: 40vw;
			height: 100%;
			align-items: center;
			justify-content: center;
		}
		nav .bg ul {
			display: flex;
			width: 40vw;
			height: 100%;
			text-align: center;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			position: static;
			gap: 2rem;
			font-size: 1.5rem;
		}
		nav .bg ul li {
			text-align: center;
			font-size: 1rem;
			margin: 0;
		}
		/* nav ul .left-side {
			display: flex;
			justify-content: space-between;
			align-items: center;
			width: 50%;
			margin-right: 3rem;
		} */
		nav .bg ul li::after {
			display: block;
			content: '';
			width: 100%;
			transform: scaleX(0);
			height: 2px;
			background-color: var(--clr-Black);
			transform-origin: bottom right;
			transition: transform 0.25s ease-out;
		}
		nav .bg ul li:hover::after {
			transform: scaleX(1);
			transform-origin: bottom left;
		}
	}
</style>
