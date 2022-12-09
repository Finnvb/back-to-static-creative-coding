<script>
	import Menu from '$lib/components/Hamburgermenu.svelte';

	let text;
	let open = false;
	let active = false;

	const toggleMenu = function () {
		active = !active;
		if (active) {
			active = true;
			open = true;
			text.style.visibility = 'hidden';
		} else {
			active = false;
			open = false;
			text.style.visibility = 'visible';
		}
	};
</script>

<header>
	<div class="home">
		<a class="centered" href="/">Home </a>
	</div>

	<h1>Stories of the <br /> ILOJO BAR</h1>

	<section>
		<div class="container" on:click={toggleMenu}>
			<span class:active />
			<span class:active />
			<span class:active />
		</div>

		<p bind:this={text}>Menu</p>
	</section>
</header>

{#if open}
	<Menu />
{/if}

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: #ffffff;
		font-size: 1.5rem;
		padding: 1rem;
	}

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	section p {
		margin-top: 0.5rem;
		font-size: 1rem;
	}
	h1 {
		font-size: 1.5rem;
		text-align: center;
	}

	a {
		text-decoration: none;
		color: rgb(118, 113, 19);
		font-size: 1.4rem;
		padding: 1.4rem;
	}

	.home {
		position: relative;
		width: 7rem;
		height: 4rem;
		background-image: url('/goldplate.png');
		background-position: center;
		background-size: contain;
		background-repeat: no-repeat;
	}
	.centered {
		position: absolute;
		top: 0;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	.container {
		position: relative;
		width: 50px;
		height: 40px;
		cursor: pointer;
		z-index: 990;
	}



	span:nth-child(1) {
		position: absolute;
		top: 0;
		transition: 0.5s;
	}

	span:nth-child(1).active {
		transform: translateY(18px) rotate(45deg);
		transform-origin: center;
	}

	.container span:nth-child(2) {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);

		transition: 0.5s;
	}

	span:nth-child(2).active {
		transform: rotateX(90deg);
		transform-origin: center;
		opacity: 0;
	}

	.container span:nth-child(3) {
		position: absolute;
		bottom: 0;
		transition: 0.5s;
	}

	.container span:nth-child(3).active {
		transform: translateY(-18px) rotate(135deg);
		transform-origin: center;
	}

	span {
		width: 100%;
		height: 5px;
		background-color: #ffffff;
		z-index: 999;
		border-radius: 1rem;
	}
</style>
