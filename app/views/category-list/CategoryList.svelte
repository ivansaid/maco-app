<stackLayout class="store-list">
    {#if selected[selected.length - 1].name.replace("Proxy<", "").replace(">", "") === "List"}
        <actionBar class="address-bar">
            <grid-layout columns="40, *" rows="*">
                <image class="address-icon" src="~/icons/truck-solid.png"/>
                <textField class="address-text" on:textChange={(val)=>{}}></textField>
            </grid-layout>
        </actionBar>
    {/if}
    <svelte:component {...props[props.length - 1]} changeComponent={addComponent} this={selected[selected.length-1]}/>
</stackLayout>


<script>
    import List from "../list/List.svelte"
    import Store from "../store/Store.svelte"

    export let changeVisibility
    export let goBackToComponent
    export let selected = [List]
    export let props = [{}]
    export let visibility = ["hidden"]


    const addComponent = (component, componentProps) => {
        switch (component) {
            case "store":
                selected = selected.concat(...selected, Store)
                props = props.concat(...props, componentProps)
                changeVisibility("visible")
                visibility = visibility.concat(...visibility, "visible")
        }
    }


</script>
=
