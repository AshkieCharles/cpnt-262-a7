<script>
	import '../app.css';
	import Header from '../lib/components/Header.svelte';
  import Weapons from 'lib/components/Card.svelte'
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
  <ul>
    {#each Weapons as {name, description, photo, external}}
      <a {external}> {name} is a {description}</a>
    {/each}
  </ul>
</section>