<script>
    import { get_current_component } from 'svelte/internal'
    import { forwardEventsBuilder } from '@smui/common/forwardEvents.js'

    export let disabled
    export let warn
    export let small
    export let ghost

    const forwardEvents = forwardEventsBuilder(get_current_component())
</script>

<button 
    use:forwardEvents
    {disabled}
    class:small
    class:warn
    class:ghost
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

    button.ghost {
        --buttonColor: var(--background);
        --buttonTextColor: var(--lineColor);
    }

    button.small {
        --buttonPadding: var(--buttonPaddingSmall);
        font-size: var(--smallText);
    }
</style>