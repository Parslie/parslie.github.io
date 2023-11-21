<script>

</script>

<div class="app">
    <!-- <header>

    </header>

    <aside>

    </aside>

    <main>

    </main> -->
    <div class="layout">
        <header>
            <h1>Viktor Holta</h1>
            <div class="corner"></div>
        </header>

        <aside>
            <div class="wrapper">
                <!-- TODO: <slot name="aside" />  -->
                <p>Aside content goes here!</p>
            </div>
            <div class="corner"></div>
        </aside>

        <main>
            <slot />
        </main>
    </div>
</div>

<style lang="scss">
    $radius: 1.5rem;
    $padding: 1rem;

    p {
        margin: 0;
    }
    
    h1 {
        margin: 0;
        line-height: 1;
    }
    
    .app {
        width: 100svw;
        min-height: 100svh;
        background-color: $background;
    }

    .layout {
        display: grid;
        grid-template-columns: 16rem 1fr;
        grid-template-rows: max-content 1fr;

        margin: 0 auto;
        max-width: 60rem;

        border-radius: $radius;
        background: linear-gradient(190deg, $primary, $accent);
    }

    header {
        grid-column: 1 / 3;
        grid-row: 1;
        position: relative;
        overflow: hidden;

        padding: $padding;
        color: $background;
    }

    aside {
        grid-column: 1;
        grid-row: 2;
        position: relative;
        overflow: hidden;

        padding: $padding;
        color: $background;
    }

    main {
        grid-column: 2;
        grid-row: 2;

        display: flex;
        flex-direction: column;
        gap: $padding;
        
        padding: $padding;

        border-top-left-radius: $radius;
        background: $background;
    }

    .corner {
        position: absolute;
        bottom: 0;
        right: 0;

        padding: $radius;
        width: 0;
        height: 0;

        border-bottom-right-radius: $radius;
        background: transparent;
        box-shadow: $radius $radius 0 0 $background;
    }

    .wrapper {
        position: sticky;
        top: 0;
        width: 100%;
    }
</style>