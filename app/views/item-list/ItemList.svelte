<listView items="{listOfItems}" on:itemTap={(item)=>{
    addComponent("store", {itemProps:item.index})
}}>
    <Template class="template-nursery" let:item>
        <Item data={item}/>
    </Template>
</listView>

<script>
    import {Template} from 'svelte-native/components'
    import Item from '../items/Items.svelte'

    export let addComponent
    let listOfItems = [1, 2, 3, 4, 5, 6, 7, 8, 9, 1, 1, 1, 1, 1, 1]
</script>
