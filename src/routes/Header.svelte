<script>
</script>

<header>
	<nav>
		<ul>
			<li>
				<a href="/">Home</a>
			</li>
			<li>
				<a href="/about">About</a>
			</li>
			<li>
				<a href="https://discord.gg/DVKypU5P3x"  target="_blank">Discord</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		width: 100%;
		justify-content: space-between;
	}

	nav {
		display: flex;
		justify-content: center;
      width: 100vw;
      --background: rgba(255, 255, 255, 0.7);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		width: 100vw;
		height: 3rem;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
		padding: 0 1rem;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1rem;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
