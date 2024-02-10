<script>
    export let title = "TODO: set title";
</script>

<article>
    <h2>{title}</h2>
    <slot />
</article>

<style lang="scss">
    article {
        border: 0.25rem solid $primary;
        border-radius: $article-radius;
        padding: 1rem;
    }

    h2 {
        line-height: 1;
        margin-bottom: 0.25em;
    }
</style>