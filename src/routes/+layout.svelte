<script>
	import '../app.css';
	import Header from '../lib/components/Header.svelte';
  import ListItem from '../lib/components/ListItem.svelte';
  import Card from '../lib/components/Card.svelte';
	
	let secList = [
		{ name: 'Ace of Spades', species: 'Dog', href: '/' },
		{ name: 'Excalibur', species: 'Cat', href: '/' },
		{ name: 'Lightsaber', species: 'Crow', href: '/' },
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
			<ListItem bgColor="bg-blue-200"><a href>
			<header><h1>{name}</h1></header>
			 is a {species} <img src="../images/Ace.png" alt=""></a></ListItem>
		{/each}
	</ul>
</section>

<Card />