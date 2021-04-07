<stackLayout class="store-list">
    {#if selected[selected.length - 1].name.replace("Proxy<", "").replace(">", "") === "List"}
        <actionBar class="address-bar">
            <grid-layout columns="40, *" rows="*">
                <image class="address-icon" src="~/icons/truck-solid.png"/>
                <textField class="address-text" on:textChange={(val)=>{}}></textField>
            </grid-layout>
        </actionBar>
    {/if}
    <svelte:component props={props[props.length - 1]} addComponent={addComponent} this={selected[selected.length-1]}/>
</stackLayout>


<script>
    import List from "../list/List.svelte"

    export let selected
    export let props
    export let addComponent
</script>

