<script>
    import { ArrowLeftIcon } from 'svelte-feather-icons'
    import { onMount } from 'svelte'

    export let size = "24"

    // TODO Get from context
    const icons = {
        back: ArrowLeftIcon
    }

    let icon

    onMount(() => icon = getIcon())

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

<svelte:component this={icon} {size} />