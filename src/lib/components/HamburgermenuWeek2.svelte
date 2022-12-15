<script>
	import { fly } from 'svelte/transition';
	import { page } from '$app/stores';

	export let width;

</script>


<section transition:fly={{ x: 1000, duration: 700 }} style="width: {width};">
	<nav>
		
		<li transition:fly={{ x: 1200, duration: 700, delay: 200 }}>
			<a
				href="/#"
				class:active={$page.url.pathname === '/a-spanish-migrant-looking-for-greener-pastures'}
				>A Spanish Migrant</a
			>
			<div></div>
			<!-- <img src="img1.jpg" alt="spanish-migrant"> -->
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 250 }}>
			<a href="/#" class:active={$page.url.pathname === '/the-returnees-who-changed-lagos'}
				>The returnees</a
			>
			<div class="img2"></div>

		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 300 }}>
			<a
				href="/#"
				class:active={$page.url.pathname === '/a-vip-from-abeokuta-visits-fernandez-house'}>A VIP</a
			>
			<div class="img3"></div>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 350 }}>
			<a href="/#" class:active={$page.url.pathname === '/the-macaulay-connection'}
				>The Macaulay connection</a
			>
			<div class="img4"></div>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 400 }}>
			<a href="/#" class:active={$page.url.pathname === '/a-family-house-to-the-olaiyas'}
				>A family house</a
			>
			<div class="img5"></div>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 450 }}>
			<a href="/#" class:active={$page.url.pathname === '/memories-of-slave-trade'}>Slave trade</a>
			<div class="img6"></div>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 500 }}>
			<a href="/#" class:active={$page.url.pathname === '/botched-dreams-for-ilojo-bar'}
				>Botched dreams</a
			>
			<div class="img7"></div>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 550 }}>
			<a href="/#" class:active={$page.url.pathname === '/the-angels-story'}>The Angel's Story</a>
			<div class="img8"></div>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 600 }}>
			<a href="/#" class:active={$page.url.pathname === '/illegal-demolition'}>Illegal demolition</a
			>
			<div class="img9"></div>
		</li>

	</nav>

</section>

<style>
	section {
		display: flex;
		justify-content: center;
		align-items: center;
		position: relative;
		background-color: var(--red);
		background-image: url('./bg1.png');
		height: 100vh;
		background-repeat: repeat;
		background-position: bottom;
		background-size: cover;
		top: 0;
		right: 0;
		width: 30vw;
		height: 100vh;
		color: #ffffff;
		z-index: 100;
		position: fixed;
	
	}

	a {
		text-decoration: none;
		color: var(--grey);
		font-size: 1.5rem;
		transition: 300ms;
	}
	a:hover {
		color: var(--light);
	}

	a.active {
		font-weight: bold;
		color: var(--redLight);
	}
	nav {
		position: absolute;
		top: 0;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
	}




	nav li div{
		visibility: hidden;
		position: absolute;
		top: 100%;
		width: 20vw;
		height: 100vh;
		background-image: url('./img1.jpg');
		background-repeat: repeat;
		background-position: bottom;
		background-size: cover;
		transition: all 0.4s ease-in-out;
		transform:translateX(-20px);
		opacity: 0%;
	}

	nav li:hover div{
	visibility: visible;
	opacity: 100%;
	transform: translateX(0px);
		
	}

	/* nav li div:last-of-type{
		right: 0;
	} */

	.img2{
		background-image: url('./img2.jpg');

	}

	.img3{
		background-image: url('./img3.jpg');
	}

	.img4{
		background-image: url('./img4.jpg');
	}

	.img5{
		background-image: url('./img5.jpg');
	}

	.img6{
		background-image: url('./img6.jpg');
	}

	.img7{
		background-image: url('./img7.jpg');
	}

	.img8{
		background-image: url('./img8.jpg');
	}

	.img9{
		background-image: url('./img9.jpg');
	}


	li {
		list-style: none;
		transition: 300ms;
		text-align: center;
		background-color: var(--red);
		padding: 1rem;
		width: 10%;
		height: 100px;
		display: flex;
		align-items: center;
		justify-content: center;
		position: relative;
		z-index: 999;
       
	}

	li:hover{
		border: 1px solid var(--grey);
		background-color: var(--redLight);
	}

   
	@media (max-width: 40rem) {
		section {
			width: 70vw;
		
		}

		nav{
			flex-direction: column;
		}

		li{
			height: 50px;
			width: 250px;
			margin: 0.5rem 0;
		}
	}
</style>
