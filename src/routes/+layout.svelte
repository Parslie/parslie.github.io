<script lang="ts">
	import { base } from "$app/paths";
	import "../global.scss";
</script>


<div class="app">
	<header>
		<span class="title">Viktor Holta</span>
		<nav>
			<a href="{base}/">About</a>
			<a href="{base}/#">Projects</a>
		</nav>
	</header>
	
	<main>
		<slot />
	</main>
</div>

<style lang="scss">
	$small-size: 0.35rem;
	$medium-size: 0.7rem;
	$large-size: 1.4rem;

	$white: #f9f9f9;
	$black: #161616;
	
	$green: #44c55b;
	$dark-green: #196c27;

	.app {
		min-height: 100vh;
		background-color: $white;
		color: $black;
	}

	header {
		display: flex;
		flex-direction: row;
		gap: $medium-size;
		align-items: center;
		
		position: sticky;
		top: 0;
		padding: $medium-size;
		width: 100vw;
		line-height: 1;

		background: linear-gradient(50deg, $green, $dark-green);
		color: $white;
		font-weight: bold;

		.title {
			font-size: 2em;
			white-space: nowrap;
			overflow: hidden;
			text-overflow: ellipsis;
		}
	}

	nav {
		display: flex;
		flex-direction: row;
		gap: $small-size;

		a {
			border-radius: $medium-size;
			border: 2px solid $white;
			padding: $small-size $medium-size;

			color: $white;
			text-decoration: none;
		}
	}

	main {
		margin: 0 auto;
		max-width: 48em;
	}
</style>