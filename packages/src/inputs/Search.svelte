<script>
    import Icon from '../Icon.svelte'

    export let search = ''
    export let placeholder = ''
    export let fitContent = false
</script>

<div class:fitContent>
    <Icon search />
    <input 
        { placeholder } 
        bind:value={search} 
        type="text" 
        name="search" 
    />
</div>

<style>
    div {
        display: flex;
        border: var(--inputBorder);
        border-radius: var(--inputBorderRadius);
        padding: var(--inputPadding);
        background: var(--inputBackground);
        box-shadow: var(--level-1);
    }

    .fitContent {
        width: fit-content;
    }

    input {
        margin-left: var(--s-1);
        background: none;
        border: none;
    }
</style>