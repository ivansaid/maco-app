<wrapLayout class="category-buttons-stack" listView>
    <button class="category-button">Nativas</button>
    <button class="category-button">Forestales</button>
    <button class="category-button">Ornamentales</button>
    <button class="category-button">Consumibles</button>
</wrapLayout>
<flexboxLayout class="flexbox-list">
    <listView items="{listOfItems}">
        <Template class="template-nursery" let:item>
           <image class="nursery-image" src="~/icons/tree-solid.png"></image>
            <label text="{item}"/>
            <label text="{item}"/>
            <label text="{item}"/>
            <label text="{item}"/>
        </Template>
    </listView>
</flexboxLayout>


<script>
    import Item from '../items/Items.svelte'
    import {Template} from 'svelte-native/components'


    let backCol = "#84A86A"

    let listOfItems = [1, 2, 3, 4, 5, 6, 7, 8, 9, 1, 1, 1, 1, 1, 1]


</script>
