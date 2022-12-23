<script>
        import '../global.css'
</script>


<main>
	<h1>Creative Coding <br>-<br> Ilojo Bar</h1>

	<section>
		<a href="/week1">Week 1 <br> Hamburgermenu Animatie</a>
		<a href="/week2">Week 2 <br> Escapism Menu</a>
		<a href="/week3">Week 3 <br> On Scroll Animation</a>
	</section>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		align-items: center;
        height: 100vh;
        /* background-color: aliceblue; */
        background-color: var(--red);
		background-image: url('/background.jpg');
		height: 100vh;
		background-repeat: repeat;
		background-position: bottom;
		background-size: cover;
	}

    h1{
        font-size: 3rem;
        color: #FFFFFF;
        text-align: center;
    
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
        width: 15rem;
        height: 7rem;
        text-align: center;
    }

    a:hover{
        transform: scale(1.1);
    }


    @media (max-width: 40em) {


   section{
    flex-direction: column;
   }
	}
</style>
