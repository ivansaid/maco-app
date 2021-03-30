<actionBar class="upper-action-bar">
    <navigationButton android.systemIcon="ic_menu_back" class="nav-button" on:tap="{goBack}" visibility={visibility}/>
    <label class="upper-action-bar-label">
        <formattedString>
            <span class="upper-action-bar-span"/>
        </formattedString>
    </label>

</actionBar>

<script>
    import {goBack} from 'svelte-native'

    export let visibility = "hidden"
</script>
