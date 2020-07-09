<style>
    :global(html) {
        font-size: var(--baseFontSize);
        box-sizing: border-box;
    }

    :global(*),
    :global(*::before),
    :global(*::after) {
        box-sizing: inherit;
    }

    :global(body) {
        font-family: var(--bodyFont);
        font-weight: 400;
        line-height: var(--lineHeight);
        background: var(--background);
        color: var(--textColor);
        padding: 0;
        margin: 0;
    }

    :global(::placeholder) {
        color: var(--gray);
    }

    :global(h1),
    :global(h2),
    :global(h3),
    :global(h4),
    :global(h5) {
        margin: 0;
        font-family: var(--headingFont);
        font-weight: 400;
        line-height: var(--lineHeight);
    }

    :global(label) {
        display: block;
        font-size: var(--smallText);
    }

    :global(p) {
        margin-bottom: 1.15rem;
        max-width: 40em;
    }

    :global(p a) {
        color: var(--textColor);
        text-decoration: none;
        border-bottom: solid 2px var(--primary);
    }
</style>

<slot></slot>