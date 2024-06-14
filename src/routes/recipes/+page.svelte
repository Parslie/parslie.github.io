<script>
	import PageLayout from '../../components/PageLayout.svelte';
	import Recipe from '../../components/Recipe.svelte';

	import pannbiff from '$lib/pannbiff_med_loksas_och_potatis.jpg';
</script>

<PageLayout>
	<p slot="aside" style="margin: 0">
		Here I describe different recipes I've used when baking or cooking, where the recipes are from,
		what I thought about them, etc.
	</p>

	<div class="recipe-list">
		<Recipe
			image={pannbiff}
			name="Pannbiff med Löksås"
			recipeUrl="pannbiff-med-lok"
			source="https://www.ica.se/recept/pannbiff-med-loksas-och-potatis-722658/"
			sourceName="ica.se"
		/><!-- TODO översätt titel till engelska? -->
	</div>
</PageLayout>

<style lang="scss">
	.recipe-list {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(20rem, 1fr));
		gap: 1rem;
	}
</style>
