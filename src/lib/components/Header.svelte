<script>
	// let text;
</script>

<header>
	<div class="home">
		<a class="centered" href="/">Home </a>
	</div>

	<h1>Stories of the <br /> ILOJO BAR</h1>

	<section />
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: #ffffff;
		font-size: 1.5rem;
		padding: 1rem;
		background-color: darkslategray;
	}

	h1 {
		text-align: center;
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

	a {
		text-decoration: none;
		color: rgb(118, 113, 19);
		font-size: 1.4rem;
		padding: 1.4rem;
	}

	@media (max-width: 40em) {
		h1 {
			font-size: 1.5rem;
		}
	}
</style>
