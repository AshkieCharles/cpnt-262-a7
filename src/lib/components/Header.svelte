<script>
	const navItems = [
		{ name: 'Home', href: '/' },
		{ name: 'About', href: '/' }
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
  }

  header {
    display: flex;
    background-color:black;
    color: white;
    justify-content: space-between;
    padding: 4px;
  }
  ul {
    display: flex;
    justify-content: space-around;
    gap: 10px;
    list-style: none;
    margin-right: 5px;
  }
  a {
    color: aliceblue;
    text-decoration: none;
  }

</style>

