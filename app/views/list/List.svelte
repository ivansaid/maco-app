<wrapLayout class="category-buttons-stack" listView>
    <button class="category-button">Nativas</button>
    <button class="category-button">Forestales</button>
    <button class="category-button">Ornamentales</button>
    <button class="category-button">Consumibles</button>
</wrapLayout>
<flexboxLayout class="flexbox-list">
    <svelte:component addComponent={addComponent} this={component}/>
</flexboxLayout>


<script>
    import ItemList from '../item-list/ItemList.svelte'

    export let addComponent
    let component = ItemList
</script>
