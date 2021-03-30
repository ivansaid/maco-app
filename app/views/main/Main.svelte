<page>
    <ActionBar/>
    <BottomBar selectedTab="{selectedTab}"/>
</page>

<script>
    import ActionBar from '../upper-bar/ActionBar.svelte'
    import BottomBar from '../bottom-navigation/BottomBar.svelte'

    const selectedTab = (value) => {
        console.log(value)
    }
</script>
