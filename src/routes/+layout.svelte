<script>
	import '../app.css';
	import Header from '../lib/components/Header.svelte';
  import Card from '../lib/components/Card.svelte';
	import Footer from '../lib/components/Footer.svelte';
	
	let secList = [
		{ name: 'Ace of Spades', species: 'Dog', href: '/', pic: 'Ace' },
		{ name: 'Excalibur', species: 'Cat', href: '/', pic: 'Excalibur' },
		{ name: 'Lightsaber', species: 'Crow', href: '/', pic: 'Lightsaber' },
	];
</script>

<Header />

<slot />

<img src="./images/Ace.png" alt="">

<style>
  img {
    overflow: hidden;
    max-width: 50vw;
  }
</style>


<section>
	<h2 class="text-3xl">Fictional Weapons</h2>
	<ul>
		{#each secList as { href, name, species }}
		<a href>
			<div class="cards">
				<header><h2>{name}</h2></header>
			<img src="../images/Lightsaber.png"alt=""> 
			<p>
				{species}
			 </p>
			</div>
		</a>

		{/each}
	</ul>
</section>

<Card />

<Footer />