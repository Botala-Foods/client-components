<script>
    export let disabled
    export let warn
    export let small
</script>

<button 
    {disabled}
    class:small
    class:warn
>
    <slot></slot>
</button>

<style>
    button {
        appearance: none;
        width: var(--buttonWidth);
        height: var(--buttonHeight);
        color: var(--buttonTextColor);
        background-color: var(--buttonColor);
        border: var(--lineThin);
        border-radius: var(--buttonBorderRadius);
        padding: var(--buttonPadding);
        box-shadow: var(--buttonShadow);
        transition: 0.3s ease-in-out box-shadow;
    }

    button:hover {
        box-shadow: var(--buttonShadowHover);
    }

    button[disabled] {
        opacity: 0.4;
    }

    button.warn {
        --buttonColor: var(--danger);
    }

    button.small {
        --buttonPadding: var(--s-1) var(--s-2);
        font-size: var(--smallText);
    }
</style>