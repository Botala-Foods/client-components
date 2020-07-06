<style>
    @font-face {
        font-family: 'Dillan';
        font-style: normal;
        font-weight: 600;
        font-display: swap;
        src: url('/dillan.woff') format('woff');
    }

    :root {
        --background: red;
    }

    :global(body) {
        background-color: var(--background);
    }

</style>

<slot></slot>