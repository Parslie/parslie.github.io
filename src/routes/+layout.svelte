<script>
    import logo from '$lib/logo.jpg';
</script>

<div class="layout">
    <header>
    </header>

    <aside>
        <div class="aside-content">
            <img class="logo" src={logo} alt="logo" />
            <h1 class="title">Viktor Holta</h1>
            <p>TODO: A short description of me.</p>
        </div>
    </aside>

    <main>
        <nav>
            <!-- TODO: create nav buttons -->
        </nav>

        <slot />
    </main>
</div>

<style lang="scss">
    $header-height: 2.5rem;
    $aside-width: 25.5rem;
    $border-radius: 1rem;
    $page-margin: max($border-radius, $header-height);

    .layout {
        background-color: $background;
        color: $text;
    }

    header {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        height: $header-height;
        background: $primary;
    }

    aside {
        position: fixed;
        top: $header-height;
        left: $page-margin;
        bottom: $page-margin;
        width: $aside-width;
        border-radius: 0 0 $border-radius $border-radius;
        background: $primary;

        .aside-content {
            position: absolute;
            top: -$header-height;
            bottom: 0;
            padding: $header-height; // TODO: make based on nav button height
        }

        &::before {
            content: "";
            position: absolute;
            top: 0;
            left: -2 * $border-radius;
            padding: $border-radius;
            border-top-right-radius: $border-radius;
            box-shadow: $border-radius (-$border-radius) 0 0 $primary;
            z-index: -1;
        }

        &::after {
            content: "";
            position: absolute;
            top: 0;
            right: -2 * $border-radius;
            padding: $border-radius;
            border-top-left-radius: $border-radius;
            box-shadow: -$border-radius (-$border-radius) 0 0 $primary;
            z-index: -1;
        }
    }

    main {
        margin: $header-height $page-margin  $page-margin ($page-margin + $aside-width);
        padding: $page-margin 0 0 $page-margin;
    }

    .logo {
        max-width: 100%;
        border-radius: 50%;
    }

    .title {
        margin: 0;
        line-height: 1;
        text-align: center;
    }
</style>