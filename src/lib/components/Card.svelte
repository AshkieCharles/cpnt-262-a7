<script>
  import {weaponList} from "../data.js";
</script>


<section>
	<h2 class="text-3xl">Fictional Weapons</h2>
	<ul>
		{#each weaponList as { href, name, description, pic, attribute}}
		<div class="cards">
			<a {href}>
				<header><h2>{name}</h2></header>
		<img src={pic} alt={attribute}>
		<p>
			{description}
		 </p>
		</a>
		</div>

		{/each}
</ul>
</section>