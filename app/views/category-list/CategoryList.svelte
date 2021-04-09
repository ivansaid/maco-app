<stackLayout class="store-list">
    {#if selected[selected.length - 1].name.replace("Proxy<", "").replace(">", "") === "List"}
        <actionBar class="address-bar">
            <grid-layout columns="68, *" rows="*">
                <button class="address-button"/>
                <image class="address-icon" src="~/icons/noun_Location_12638.png"/>
                <textField class="address-text" on:textChange={(val)=>{}}></textField>
            </grid-layout>
        </actionBar>
    {/if}
    <svelte:component addComponent={addComponent} props={props[props.length - 1]} this={selected[selected.length-1]}/>
</stackLayout>


<script>
    import List from "../list/List.svelte"

    export let selected
    export let props
    export let addComponent
</script>

