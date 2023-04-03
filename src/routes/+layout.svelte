<script>
	import { base } from '$app/paths';
</script>

<div>
	<header>
		<h1>Viktor Holta</h1>
		<nav>
			<a href="{base}/">About</a>
		</nav>
	</header>

	<main>
		<slot />
	</main>

	<footer>
		<h4>Viktor Holta <b>©</b> 2023</h4>
	</footer>
</div>

<style lang="scss">
	
</style>
