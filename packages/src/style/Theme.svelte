<script>
    import NormalizeCSS from 'svelte-normalize-css'
    import StyleBase from './StyleBase.svelte'
    import ThemeBase from './ThemeBase.svelte'
</script>

<NormalizeCSS>
    <StyleBase>
        <ThemeBase>
            <slot></slot>
        </ThemeBase>
    </StyleBase>
</NormalizeCSS>