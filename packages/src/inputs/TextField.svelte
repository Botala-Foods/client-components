<script>
    export let value
    export let placeholder = ''
</script>

<input type="text" bind:value { placeholder } />

<style>
    input {
        padding: var(--inputPadding);
        border: var(--inputBorder);
        border-radius: var(--inputBorderRadius);
        background: var(--inputBackground);
    }
</style>