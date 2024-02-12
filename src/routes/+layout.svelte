<script>
    import logo from '$lib/logo.jpg';
</script>

<div class="layout">
    <header>
        <aside>
            <img class="logo" src={logo} alt="logo" />
            <h1 class="title">Viktor Holta</h1>

            <nav>
                <a href="/">Home</a>
                <a href="/programming">Programming</a>
                <a href="/modeling">3D modeling</a>
            </nav>
        </aside>
    </header>
    
    <main>
        <slot />
    </main>
</div>

<style lang="scss">
    $aside-width: 23rem;

    .layout {
        position: absolute;
        top: 0;
        width: 100vw;
        min-height: 100vh;
        background-color: $background;
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
            padding: 0 $aside-padding $aside-padding;
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

    nav {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        margin-top: 0.5rem;

        a {
            border: 0.125rem solid $background;
            border-radius: $nav-button-radius;
            text-align: center;
            color: $text;
            background-color: darken($primary, 12%);
            text-decoration: none;
            font-weight: bold;

            &:hover {
                background-color: darken($primary, 18%);
            }
        }
    }

    main {
        display: flex;
        flex-direction: column;
        gap: $layout-padding;
        position: relative; // Needed to make content interactable
        margin: ($layout-padding + $layout-border) $layout-padding $layout-padding ($aside-width + $layout-padding * 2);
    }
    
    .logo {
        max-width: 100%;
        border-radius: $nav-button-radius;
    }

    .title {
        text-align: center;
    }
</style>