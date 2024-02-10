<script>
    export let items = [];
</script>

<div class="list">
    {#each items as [duration, title, location]}
        <div class="item">
            <span class="title">{title}</span>
            <span class="location">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512">
                    <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
                    <path d="M215.7 499.2C267 435 384 279.4 384 192C384 86 298 0 192 0S0 86 0 192c0 87.4 117 243 168.3 307.2c12.3 15.3 35.1 15.3 47.4 0zM192 128a64 64 0 1 1 0 128 64 64 0 1 1 0-128z"/>
                </svg>
                {location}
            </span>
            <span class="duration">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
                    <path d="M256 0a256 256 0 1 1 0 512A256 256 0 1 1 256 0zM232 120V256c0 8 4 15.5 10.7 20l96 64c11 7.4 25.9 4.4 33.3-6.7s4.4-25.9-6.7-33.3L280 243.2V120c0-13.3-10.7-24-24-24s-24 10.7-24 24z"/>
                </svg>
                {duration}
            </span>
        </div>
    {/each}
</div>

<style lang="scss">
    .list {
        display: flex;
        flex-direction: column;
    }

    .item {
        display: grid;
        grid-template-columns: max-content 1fr;
        grid-template-rows: max-content max-content;
        column-gap: 1ch;
        row-gap: 0.5em;
        padding: 0.5rem;
        line-height: 1;
        border-radius: $content-radius;
        &:nth-child(odd) {
            background-color: lightgray;
        }

        .title {
            grid-column: 1 / 3;
            font-weight: bold;
        }
    }

    svg {
        display: inline;
        height: 1em;
        vertical-align: bottom;
    }
</style>