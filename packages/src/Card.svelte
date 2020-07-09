<script>
    import { get_current_component } from 'svelte/internal'
    import { forwardEventsBuilder } from '@smui/common/forwardEvents.js'
    import Flex from './utils/Flex.svelte'

    const forwardEvents = forwardEventsBuilder(get_current_component())
</script>

<div class='card' use:forwardEvents>
    <div class='title'>
        <slot name='title' />
        <Flex>
            <slot name='title-center' />
        </Flex>
    </div>
    <slot></slot>
</div>

<style>
    .card {
        padding: var(--cardPadding);
        background: var(--cardBg);
        box-shadow: var(--cardShadow);
        border: var(--line);
        border-radius: var(--borderRadius);
    }

    .card > *:first-child, .title {
        margin-top: var(--cardFirstChildMarginTop);
    }

    .card > *:last-child {
        margin-bottom: var(--cardLastChildMarginBottom);
    }
</style>
