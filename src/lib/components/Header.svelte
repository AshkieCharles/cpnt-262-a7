<script>
	const navItems = [
		{ name: 'Home', href: '/' },
		{ name: 'About', href: '/' },
    { name: 'Contact Us', href: '/' },
    { name: 'Donate', href: '/' }
	];
</script>

<header>
	<nav>
		<ul>
			{#each navItems as { name, href }}
				<li><a {href}>{name}</a></li>
			{/each}
		</ul>
	</nav>
</header>

<style>
  nav {
    display: flex;
    margin: auto;
  }

  header {
    display: flex;
    background-color:black;
    color: white;
    padding: 4px;
  }
  ul {
    display: flex;
    justify-content: space-around;
    gap: 10rem;
    list-style: none;
    margin-right: 5px;
  }
  a {
    color: aliceblue;
    text-decoration: none;
  }

</style>

