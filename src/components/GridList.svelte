<div>
  <slot />
</div>

<style lang="scss">
	$small-size: 0.35rem;
	$medium-size: 0.7rem;
	$large-size: 1.4rem;

	$white: #f9f9f9;
	$black: #161616;
	
	$green: #44c55b;
	$dark-green: #196c27;
  
  div {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(8ch, 1fr));
    column-gap: $large-size;
    row-gap: $small-size;
    margin: $medium-size 0;
    justify-items: center;
    align-items: center;

    &:first-child { margin-top: 0; }
    &:last-child { margin-bottom: 0; }
  }
</style>