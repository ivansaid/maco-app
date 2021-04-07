<actionBar class="upper-action-bar">
    <navigationButton android.systemIcon="ic_menu_back" class="nav-button" on:tap="{()=>{}}"
                      visibility={visibility}/>
    <image class="address-icon-bar" src="~/icons/maco_name.png"/>
</actionBar>

<script>
    export let visibility = "hidden"
</script>

