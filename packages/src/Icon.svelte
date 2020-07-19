<script>
    import { ArrowLeftIcon, PlusCircleIcon, BellIcon, SettingsIcon } from 'svelte-feather-icons'
    import { onMount } from 'svelte'
    import { get_current_component } from 'svelte/internal'
    import { forwardEventsBuilder } from '@smui/common/forwardEvents.js'

    export let small
    export let medium
    export let large

    const forwardEvents = forwardEventsBuilder(get_current_component())

    // TODO Get from context
    const icons = {
        back: ArrowLeftIcon,
        settings: SettingsIcon,
        notifications: BellIcon,
        plusCircle: PlusCircleIcon,
    }

    let icon, size 
    
    onMount(() => {
        size = `${getSize()}`
        icon = getIcon()
    })

    const getSize = () => {
        let baseFontSize = getComputedStyle(document.documentElement).getPropertyValue('--baseFontSize')
        baseFontSize = +(baseFontSize.substring(0, baseFontSize.indexOf('px')))

        if (small) return baseFontSize * 1
        if (medium) return baseFontSize * 2
        if (large) return baseFontSize * 3
        return baseFontSize * 1.5
    }

    const getIcon = () => {
        const prop = Object.keys($$restProps)[0]

        try {
            if (icons[prop]) return icons[prop]
            throw Error('User icons not specified')
        } catch (error) {
            console.error(`Could not find icon [${prop}]: `, error)
        }
    }
</script>

{#if icon}
    <div 
        class="wrapper"
        use:forwardEvents
    >
        <svelte:component this={icon} {size} />
    </div>
{/if}