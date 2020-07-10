<script>
    import { ArrowLeftIcon } from 'svelte-feather-icons'
    import { onMount } from 'svelte'

    export let small
    export let medium
    export let large

    // TODO Get from context
    const icons = {
        back: ArrowLeftIcon
    }

    let icon, size 
    
    onMount(() => {
        size = `${getSize()}`
        icon = getIcon()
    })

    const getSize = () => {
        debugger
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
    <svelte:component this={icon} {size} />
{/if}