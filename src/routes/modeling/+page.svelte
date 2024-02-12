<script>
    import Article from "../../components/Article.svelte";
    import kallax from "$lib/kallax-4x4.webp";
    import malm from "$lib/malm.webp";
</script>

<Article title="Notice">
    <p>
        I'm planning on uploading my models somewhere else (maybe on sketchfab), so that they're not just static images.
    </p>
</Article>

<Article title="Kallax 4x4">
    <img src={kallax} alt="kallax 4 by 4 bookshelf" />
</Article>

<Article title="Malm">
    <img src={malm} alt="malm drawer" />
</Article>

<style lang="scss">
    img {
        display: block;
        max-width: 100%;
        border-radius: $content-radius;
    }
</style>