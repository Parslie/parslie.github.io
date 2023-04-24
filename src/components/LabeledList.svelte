<script lang="ts">
  export let items: LabeledListItem[];
  export let title: string | undefined = undefined;
</script>

<script lang="ts" context="module">
  export type LabeledListItem = [string, string];
</script>

<div>
  {#if title}
    <span class="title">{title}</span>
  {/if}
  {#each items as item}
    <span class="label">{item[0]}</span>
    <span class="content">{item[1]}</span>
  {/each}
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
    grid-template-columns:  max-content 1fr;
    column-gap: $large-size;
    row-gap: $small-size;
    margin: $medium-size 0;

    &:first-child { margin-top: 0; }
    &:last-child { margin-bottom: 0; }

    .title {
      font-weight: bold;
      grid-column: 1 / span 2;
    }

    .label {
      font-weight: bold;
    }
  }
</style>