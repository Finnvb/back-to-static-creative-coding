<script>
	import { fly } from 'svelte/transition';
	import { page } from '$app/stores';

	export let width;
    // export let visible;
</script>

<section transition:fly={{ x: 1000, duration: 700 }} style="width: {width};">
	<nav>
		<li onmouseover="console.log('gfgg')" transition:fly={{ x: 1200, duration: 700, delay: 200 }}>
			<a
				href="/#"
				class:active={$page.url.pathname === '/a-spanish-migrant-looking-for-greener-pastures'}
				>A Spanish Migrant</a
			>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 250 }}>
			<a href="/#" class:active={$page.url.pathname === '/the-returnees-who-changed-lagos'}
				>The returnees</a
			>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 300 }}>
			<a
				href="/#"
				class:active={$page.url.pathname === '/a-vip-from-abeokuta-visits-fernandez-house'}>A VIP</a
			>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 350 }}>
			<a href="/#" class:active={$page.url.pathname === '/the-macaulay-connection'}
				>The Macaulay connection</a
			>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 400 }}>
			<a href="/#" class:active={$page.url.pathname === '/a-family-house-to-the-olaiyas'}
				>A family house</a
			>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 450 }}>
			<a href="/#" class:active={$page.url.pathname === '/memories-of-slave-trade'}>Slave trade</a>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 500 }}>
			<a href="/#" class:active={$page.url.pathname === '/botched-dreams-for-ilojo-bar'}
				>Botched dreams</a
			>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 550 }}>
			<a href="/#" class:active={$page.url.pathname === '/the-angels-story'}>The Angel's Story</a>
		</li>
		<li transition:fly={{ x: 1200, duration: 700, delay: 600 }}>
			<a href="/#" class:active={$page.url.pathname === '/illegal-demolition'}>Illegal demolition</a
			>
		</li>
	</nav>
	<!-- <img class="li-image" class:visible src="spanish-migrant.jpg" alt="red" /> -->
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		align-items: center;
		position: relative;
		background-color: var(--red);
		background-image: url('/bg1.png');
		opacity: 10%;
		height: 100vh;
		/* width: 100vw; */
		background-repeat: repeat;
		background-position: bottom;
		background-size: cover;
		top: 0;
		right: 0;
		width: 30vw;
		height: 100vh;
		color: #ffffff;
		opacity: 100;
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
        z-index: 999;
	}
	li {
		list-style: none;
		/* margin: 0.5rem 0; */
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
       
	}

    li:nth-child(1){
        border-radius: 0 0 0 20px;
    }

    li:last-child{
        border-radius: 0 0 20px 0;
    }

    /* li:hover ~ .li-image {
  display: block;  
}
    .li-image{
        position: absolute;
        width: 40vw;
        height: 100vh;
       display: none;
    } */

	/* .red{
    position: absolute;
   width: 100px;
   height: 200px;
   background-color: aliceblue;
   bottom: 0;
   left: 0;
   margin-left: 7rem;
   animation: orb 1.8s infinite;
}

@keyframes orb {
	0%,100% {
		box-shadow: 0 0 5px 2px #8FFFCF;
	}
	50% {
		box-shadow: 0 0 24px 4px #8FFFCF;
	}
} */
	@media (max-width: 40rem) {
		section {
			width: 70vw;
		}
	}
</style>
