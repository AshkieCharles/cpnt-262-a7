<script>
	import '../app.css';
	import Header from '../lib/components/Header.svelte';

  import Card from '../lib/components/Card.svelte';
	import Footer from '../lib/components/Footer.svelte';
	
	let secList = [
		{ name: 'Ace of Spades', description: 'Ace of Spades is an exotic hand cannon introduced in Destiny 2: Forsaken. Ace of Spades is the trusty Hand Cannon of Cayde-6, and was built specifically for him by Banshee-44. The gun is taken by Uldren Sov in the events of Forsaken. Uldren Sov uses it to kill Cayde-6. This weapon is later claimed by the Guardian.', href: 'https://destiny.fandom.com/wiki/Ace_of_Spades_(Destiny_2)', image:'Ace'
		, external: "" },
		{ name: 'Excalibur', description: 'the strongest and most majestic holy sword that symbolizes King Arthur. As that which can be called the physical actualization of her ideals and the symbol of her heroism, it is her greatest and most powerful Noble Phantasm. Its power is said to be rivaled by Rhongomyniad.[6]', href: 'https://typemoon.fandom.com/wiki/Excalibur', pic: 'Excalibur', external: "" },
		{ name: 'Lightsaber', description: 'The lightsaber, also referred to as a laser sword by those who were unfamiliar with it, was a weapon usually used by the Jedi, Sith, and other Force-sensitives. Lightsabers consisted of a plasma blade, powered by a kyber crystal, that was emitted from a usually metal hilt and could be shut off at will. It was a weapon that required skill and training, and was greatly enhanced when used in conjunction with the Force. Though also used by the Sith, the lightsaber was synonymous with the Jedi, with some in the galaxy believing only Jedi could use lightsabers.', href: 'https://starwars.fandom.com/wiki/Lightsaber', pic: 'Lightsaber', external: ""},
	];
</script>

<slot />



<style>
  img {
    overflow: hidden;
    max-width: 50vw;
  }
</style>


<section>
	<h2 class="text-3xl">Fictional Weapons</h2>
	<ul>
		{#each secList as { href, name, description}}
		<a {href}>
				<div class="cards">
						<header><h2>{name}</h2></header>
				<img src="../images/Lightsaber.png"alt="">
				
				<p>
						{description}
				 </p>
				</div>
		</a>

		{/each}
</ul>
</section>


<Card />
<Footer />
