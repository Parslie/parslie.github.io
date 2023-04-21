<script lang="ts">
	import { base } from '$app/paths';
	import '../global.scss';
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
		max-width: 56rem;
	}
</style>

<!--
	<script lang="ts">
	import { base } from '$app/paths';
	import { onMount } from 'svelte';
	import '../global.scss';

	let onScroll = () => false;
	let scrollY: number;
	$: isScrolled = scrollY != -1 && onScroll();

	onMount(() => {
		onScroll = () => {
			const nav = document.getElementsByTagName('nav')[0];
			const navRect = nav.getBoundingClientRect();
			return navRect.top === 0;
		}
	});
</script>

<svelte:window bind:scrollY={scrollY} />

<div class="app">
	<header>
		<span>Viktor Holta</span>
	</header>

	<nav>
		<a href="{base}/">About</a>
		<a href="{base}/#">Projects</a>
	</nav>

	<main>
		<slot />
	</main>

	<footer>
		<span>Viktor Holta <b>©</b> 2023</span>
	</footer>
</div>

<style lang="scss">
	$small-size: 0.4rem;
	$medium-size: 0.8rem;
	$large-size: 1.6rem;

	$white: #fafafa;
	$light-gray: #eaeaea;
	$gray: #aaaaaa;
	$black: #111111;

	$green: #44c55b;
	$dark-green: #196c27;

	.app {
		display: flex;
		flex-direction: column;

		min-height: 100vh;
		
		background: $light-gray;
		color: $black;

		header {
			margin: 0 auto;
			padding: $medium-size;
			max-width: 100vw;
			width: 50rem;

			font-size: 3em;
			font-weight: bold;
			text-align: center;
		}

		nav {
			display: flex;
			flex-direction: row;

			position: relative;
			margin: 0 auto;
			border: 1px solid $gray;
			border-top: 0;
			border-bottom: 0;
			max-width: 100vw;
			width: 50rem;

			background: linear-gradient(0deg, $white, $light-gray);

			&::before {
				content: '';
				position: absolute;
				left: -1px;
				top: 0;
				bottom: 0;
				width: 1px;
				background: linear-gradient(0deg, transparent, $light-gray);
			}

			&::after {
				content: '';
				position: absolute;
				right: -1px;
				top: 0;
				bottom: 0;
				width: 1px;
				background: linear-gradient(0deg, transparent, $light-gray);
			}

			a {
				padding: $medium-size;

				color: $black;
				font-weight: bold;
				text-decoration: none;

				&:hover { color: $gray; }
			}
		}

		main {
			margin: 0 auto;
			border: 1px solid $gray;
			border-top: 0;
			padding: $medium-size;
			max-width: 100vw;
			width: 50rem;
			
			background: $white;
		}

		footer {
			margin: 0 auto;
			padding: $medium-size;
			max-width: 100vw;
			width: 50rem;
		}
	}
</style>

-->