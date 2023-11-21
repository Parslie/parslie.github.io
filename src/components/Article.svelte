<div class="wrapper">
    <article>
        <h2>
            article
        </h2>
        <p>
            bottom text
        </p>
    </article>
</div>

<style lang="scss">
    $radius: 0.75rem;
    $border-width: 3px;
    
    p {
        margin: 0;
    }

    h2 {
        margin: 0;
        line-height: 1;
    }

    .wrapper {
        padding: $border-width;
        border-radius: $radius;
        background: linear-gradient(190deg, $primary, $accent);
    }

    article {
        padding: 1rem;
        
        border-radius: calc($radius - $border-width);
        background: $background;
    }
</style>