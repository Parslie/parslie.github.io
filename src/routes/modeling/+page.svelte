<script>
    import Article from "../../components/Article.svelte";
</script>

<Article title="Notice">
    <p>
        I'm planning on uploading my models somewhere else (maybe on sketchfab), so that they're not just static images.
    </p>
</Article>

<div class="model-grid">
    <Article title="Kallax 4x4">
        <div class="sketchfab-embed-wrapper">
            <iframe title="kallax-4x4" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/f10f30205f5445b597e7b62dcc3d3b9c/embed?camera=0"></iframe>
        </div>
    </Article>
    
    <Article title="Malm">
        <div class="sketchfab-embed-wrapper">
            <iframe title="Malm" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/63aeb77e3ed44d398b7a9807189718a8/embed?camera=0"></iframe>
        </div>
    </Article>
</div>

<style lang="scss">
    img {
        display: block;
        max-width: 100%;
        border-radius: $content-radius;
    }

    .model-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(32rem, 1fr));
        gap: $layout-padding;
    }
    
    .sketchfab-embed-wrapper iframe {
        display: block;
        width: 100%;
        aspect-ratio: 10/7;
        border-radius: $content-radius;
    }
</style>