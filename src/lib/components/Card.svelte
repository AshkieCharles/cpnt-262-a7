<script>
  import {weaponList} from "../data.js";
</script>


<section>
	<h2 class="text-3xl">Fictional Weapons</h2>
	<ul>
		{#each weaponList as { href, name, description, pic, attribute}}
		<a {href}>
				<div class="cards">
						<header><h2>{name}</h2></header>
				<img src={pic} alt={attribute}>
				<p>
					{description}
				 </p>
				</div>
		</a>

		{/each}
</ul>
</section>