<div class="article-wrapper">
	<article>
		<slot />
	</article>
</div>

<style lang="scss">
	$small-size: 0.35rem;
	$medium-size: 0.7rem;
	$large-size: 1.4rem;

	$white: #f9f9f9;
	$black: #161616;
	
	$green: #44c55b;
	$dark-green: #196c27;
  
  .article-wrapper {
		margin: $large-size 0;
		border-radius: $medium-size;
		padding: 2px;

		background: linear-gradient(50deg, $green, $dark-green);
  }

	article {
		border-radius: calc($medium-size - 2px); // Subtracts .article-wrapper padding
    padding: $medium-size;
		
		background: $white;
	}
</style>