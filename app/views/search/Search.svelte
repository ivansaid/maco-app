<stackLayout backgroundColor="white">
    <actionBar class="address-bar">
        <grid-layout columns="70, *" rows="*">
            <textField class="search-text" on:textChange={(val)=>{}}></textField>
            <button class="button-search">buscar</button>
        </grid-layout>
    </actionBar>
    {#if selected[selected.length - 1].name.replace("Proxy<", "").replace(">", "") === "SearchExample"}
        <SearchExample/>
    {/if}
</stackLayout>


<script>
    import SearchExample from "../search/SearchExample.svelte"

    export let selected
    export let props
    export let addComponent
</script>
