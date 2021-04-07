<page>
    <ActionBar visibility={visibility}/>
    <BottomBar changeVisibility={changeVisibility}/>
</page>

<script>
    import ActionBar from '../upper-bar/ActionBar.svelte'
    import BottomBar from '../bottom-navigation/BottomBar.svelte'


    let visibility = "hidden"
    const changeVisibility = (v) => {
        visibility = v
    }
</script>
