<script>
	import '../app.css';
	import Header from '../lib/components/Header.svelte';
  import ListItem from '../lib/components/ListItem.svelte';
  import Card from '../lib/components/Card.svelte';
	
	let secList = [
		{ name: 'Alfred', species: 'Dog', href: '/' },
		{ name: 'Elvira', species: 'Cat', href: '/' },
		{ name: 'Sally', species: 'Crow', href: '/' },
		{ name: 'Gus', species: 'Ferret', href: '/' }
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
	<h2 class="text-3xl">Mythical Weapons</h2>
	<ul>
		{#each secList as { href, name, species }}
			<ListItem bgColor="bg-blue-200"><a {href}>{name} is a {species} </a></ListItem>
		{/each}
	</ul>
</section>

<Card />