<stackLayout backgroundColor="white">
    <actionBar class="address-bar">
        <grid-layout columns="68, *" rows="*">
            <textField class="search-text" on:textChange={(val)=>{}}></textField>
            <button class="button-search"/>
            <image class="address-icon" src="~/icons/noun_Location.png"/>
        </grid-layout>
    </actionBar>
    {#if selected[selected.length - 1].name.replace("Proxy<", "").replace(">", "") === "SearchExample"}
        <SearchExample/>
    {/if}
</stackLayout>


<script>
    import SearchExample from "../messages/SearchExample.svelte"

    export let selected
    export let props
    export let addComponent
</script>
