<script context="module">
    let counter = 0
</script>

<script>
    import { onMount } from "svelte"
    import feather from 'feather-icons'

    export let f = true // Feather icon

    // TODO Get from context
    const icons = []
    let icon 
    let container
    let _class 

    onMount(() => {
        icon = getIcon()
    })

    const getIcon = () => {
        const prop = Object.keys($$restProps)[0]

        try {
            if (f) {
                _class = `icon${counter++}`
                return feather.icons[prop].toSvg({ class: _class })
            } 
            
            throw Error('User icons not specified')
        } catch (error) {
            console.error(`Could not find icon [${prop}]: `, error)
        }
    }
</script>

{@html icon}