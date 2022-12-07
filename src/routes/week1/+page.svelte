<script>
	import Menu from '$lib/components/HamburgerMenu.svelte';
	let close;
	let openImg;
	let text;
	let active = false;
	export let open = false;
	export let closeMenu = () => {
		// close.style.display = 'none';
		// openImg.style.display = 'flex';
		// text.style.visibility = 'hidden';
		open = true;
		active = true;
	};
	export let openMenu = () => {
		// openImg.style.display = 'none';
		// close.style.display = 'flex';
		// text.style.visibility = 'visible';
		open = false;
        active = false
	};
</script>

<header>
	<div class="home">
		<a class="centered" href="/">Home </a>
	</div>

	<h1>Stories of the <br /> ILOJO BAR</h1>

	<div class="container" on:click={closeMenu} >
		<span class:active/>
		<span class:active/>
		<span class:active/>
	</div>
	<!-- <div class="container">
			<img bind:this={close} on:click={closeMenu} src="close.svg" alt="closeImg" />
			<img
				class="close"
				bind:this={openImg}
				on:click={openMenu}
				src="hamburgerMenu.svg"
				alt="hamburgerImg"
			/>
		</div> -->
	<!-- <p bind:this={text}>Menu</p> -->
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
		transition: 1s;
        z-index: 990;
	}

	span:nth-child(1) {
		position: absolute;
		top: 0;
		transition: 1s;
	}

	span:nth-child(1).active {
		/* transform: translateY(18px); */
		transform: translateY(18px) rotate(45deg);
		/* transform-origin: center; */
	}

	.container span:nth-child(2) {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);

		transition: 1s;
	}

	span:nth-child(2).active {
		display: none;
		transform: translateX(20px);
	}

	.container span:nth-child(3) {
		position: absolute;
		bottom: 0;
		/* transform: translateY(-18px); */
		transition: 1s;
	}

	.container span:nth-child(3).active {
		/* transform: translateY(-18px); */
		transform: translateY(-18px) rotate(135deg);
		transform-origin: center;
	}

	span {
		/* position: absolute; */
		width: 100%;
		height: 5px;
		background-color: #ffffff;
		z-index: 999;
		border-radius: 1rem;
	}
</style>
