<script>
        import '../global.css'
</script>


<main>
	<h1>Creative Coding</h1>

	<section>
		<a href="/week1">Week 1</a>
		<a href="/">Week 2</a>
		<a href="/">Week 3</a>
	</section>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		align-items: center;
        height: 100vh;
        background-color: aliceblue;
	}

    h1{
        font-size: 3rem;
    }

	section {
		display: flex;
		flex-direction: row;
		justify-content: center;
        gap: 4rem;
		align-items: flex-start;
	}

    a{
        padding: 2rem;
        border-radius: 1rem;
        background-color:maroon;
        text-decoration: none;
        color: aliceblue;
        transition: 0.5s;
        font-weight: bold;
    }

    a:hover{
        transform: scale(1.1);
    }
</style>
