<script>
	import IntersectionObserver from 'svelte-intersection-observer';
	import { fade } from 'svelte/transition';
	import { fly } from 'svelte/transition';

	import Header from '$lib/components/Header.svelte';

	let p1;
	let p2;
	let p3;
	let img;
	let img2;
</script>

<Header />
<main>
	<IntersectionObserver element={p1} let:intersecting >
		<div bind:this={p1}>
			{#if intersecting}
				<p transition:fly={{ x: 1000, duration: 1700 }}>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores nam atque sequi autem
					itaque. Quas, libero asperiores. Dolorem quasi quaerat magni ea, facere repellendus quo
					facilis nemo mollitia deserunt fugiat voluptatem laboriosam dignissimos incidunt nisi
					nobis? Ipsum quidem unde vel accusamus facilis beatae eos sunt, aperiam vitae, nisi quasi.
					Amet, reiciendis! Ex tenetur, odit quod quibusdam facilis eos debitis nobis optio quos
					soluta nostrum! Esse sit eveniet repudiandae consequuntur quam maiores reiciendis, dicta
					similique nam qui fuga, perspiciatis autem at illum? Accusantium temporibus, quasi dolorum
					cupiditate doloribus blanditiis voluptatem architecto veniam maxime a rem sunt asperiores
					fugit quia laboriosam aspernatur!
				</p>
			{/if}
		</div>
	</IntersectionObserver>

	<IntersectionObserver element={img} let:intersecting >
		<div bind:this={img}>
			{#if intersecting}
            <div>
				<img transition:fly={{ x: -1000, duration: 1700 }} src="img1.jpg" alt="test" />
            </div>
			{/if}
		</div>
	</IntersectionObserver>

	<IntersectionObserver element={p2} let:intersecting >
		<div bind:this={p2}>
			{#if intersecting}
				<p transition:fly={{ x: 1000, duration: 1700 }}>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores nam atque sequi autem
					itaque. Quas, libero asperiores. Dolorem quasi quaerat magni ea, facere repellendus quo
					facilis nemo mollitia deserunt fugiat voluptatem laboriosam dignissimos incidunt nisi
					nobis? Ipsum quidem unde vel accusamus facilis beatae eos sunt, aperiam vitae, nisi quasi.
					Amet, reiciendis! Ex tenetur, odit quod quibusdam facilis eos debitis nobis optio quos
					soluta nostrum! Esse sit eveniet repudiandae consequuntur quam maiores reiciendis, dicta
					similique nam qui fuga, perspiciatis autem at illum? Accusantium temporibus, quasi dolorum
					cupiditate doloribus blanditiis voluptatem architecto veniam maxime a rem sunt asperiores
					fugit quia laboriosam aspernatur!
				</p>
			{/if}
		</div>
	</IntersectionObserver>

	<IntersectionObserver element={img2} let:intersecting >
		<div bind:this={img2}>
			{#if intersecting}
            <div>
				<img transition:fly={{ x: -1000, duration: 1700 }} src="img2.jpg" alt="test" />
            </div>
			{/if}
		</div>
	</IntersectionObserver>

	<IntersectionObserver element={p3} let:intersecting >
		<div bind:this={p3}>
			{#if intersecting}
				<p transition:fly={{ x: 1000, duration: 1700 }}>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores nam atque sequi autem
					itaque. Quas, libero asperiores. Dolorem quasi quaerat magni ea, facere repellendus quo
					facilis nemo mollitia deserunt fugiat voluptatem laboriosam dignissimos incidunt nisi
					nobis? Ipsum quidem unde vel accusamus facilis beatae eos sunt, aperiam vitae, nisi quasi.
					Amet, reiciendis! Ex tenetur, odit quod quibusdam facilis eos debitis nobis optio quos
					soluta nostrum! Esse sit eveniet repudiandae consequuntur quam maiores reiciendis, dicta
					similique nam qui fuga, perspiciatis autem at illum? Accusantium temporibus, quasi dolorum
					cupiditate doloribus blanditiis voluptatem architecto veniam maxime a rem sunt asperiores
					fugit quia laboriosam aspernatur!
				</p>
			{/if}
		</div>
	</IntersectionObserver>
</main>

<style>
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		gap: 10rem;
		background-color: darkslategrey;
       
	}

	p {
		width: 30vw;
		color: white;
		display: block;
		padding: 1rem;
	}

	img {
		width: 30vw;
		display: block;
	}

    @media (max-width: 40em) {
	p{width: 20em;}

    img{width: 20em;}
	}

</style>
