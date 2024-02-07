<script>
    export let title = "TODO: set title";
</script>

<article>
    <h2>{title}</h2>
    <slot />
</article>

<style lang="scss">
    article {
        :first-child { margin-top: 0; }
        :last-child { margin-bottom: 0; }

        border: $small solid $primary;
        border-radius: $large;
        padding: $large;
        box-sizing: border-box;
    }
</style>