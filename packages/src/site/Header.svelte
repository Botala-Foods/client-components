<script>
    export let logoImage
    export let links = [
        {
            href: '/about',
            label: 'about'
        }
    ]
</script>

<header>
    <img src="{logoImage}" alt="">
    <nav>
        {#each links as { href, label }}
            <a {href}>{label}</a>
        {/each}
    </nav>
</header>

<style>
    header {
        position: fixed;
        left: 0;
        top: 0;
        width: calc(100% - (var(--headerMarginX) * 2));
        height: var(--headerHeight);
        background: var(--headerBackground);
        border: var(--line);
        border-radius: var(--borderRadius);
        margin-top: var(--headerMarginY);
        margin-left: var(--headerMarginX);
        margin-right: var(--headerMarginX);
        box-shadow: var(--headerShadow);
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 var(--containerPadding);
    }

    header nav a {
        color: var(--headerLinkColor);
        text-decoration: none;
    }

    header nav a + a {
        margin-left: 10px;
    }
</style>