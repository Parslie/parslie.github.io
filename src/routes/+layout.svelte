<script>
    import logo from '$lib/logo.jpg';
</script>

<div class="layout">
    <header>
        <aside>
            <img class="logo" src={logo} alt="logo" />
            <h1 class="title">Viktor Holta</h1>
            <p>TODO: A short description of me.</p>
        </aside>
    </header>

    <main>
        <slot />
    </main>
</div>

<style lang="scss">
    $aside-width: 23rem;

    .layout {
        color: $text;
    }

    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        border-top: $layout-border solid $primary;

        aside {
            position: relative;
            top: 0;
            left: $layout-padding;
            width: $aside-width;
            max-height: calc(100vh - $layout-padding - $layout-border);
            padding: 0 1rem 1rem;
            background-color: $primary;
            border-radius: 0 0 $layout-radius $layout-radius;

            &::before, &::after {
                content: "";
                position: absolute;
                top: 0;
                padding: $layout-radius;
                background-color: transparent;
                box-shadow: 0 (-$layout-radius) 0 0 $primary;
            }

            &::before {
                left: -2 * $layout-radius;
                border-top-right-radius: $layout-radius;
            }

            &::after {
                right: -2 * $layout-radius;
                border-top-left-radius: $layout-radius;
            }
        }
    }

    main {
        display: flex;
        flex-direction: column;
        gap: $layout-padding;
        margin: ($layout-padding + $layout-border) $layout-padding $layout-padding ($aside-width + $layout-padding * 2);
    }

    .logo {
        max-width: 100%;
    }
</style>