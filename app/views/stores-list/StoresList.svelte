<flexbox-layout class="store-list">
    <actionBar class="address-bar">
        <grid-layout columns="40, *" rows="*">
            <image class="address-icon" src="~/icons/truck-solid.png"/>
            <textField class="address-text"  on:textChange={(val)=>{}}></textField>
        </grid-layout>
    </actionBar>
    <scrollView alignSelf="center" orientation="vertical">
        <flexboxLayout alignItems="center" flexWrap="wrap" justifyContent="space-evenly"
                       marginLeft="5"
                       marginRight="5">
            <Item/>
            <Item/>
            <Item/>
            <Item/>
            <Item/>
            <Item/>
        </flexboxLayout>
    </scrollView>
</flexbox-layout>center


<script>
    import {navigate} from "svelte-native";
    import Store from "../store/Store.svelte";
    import {Template} from 'svelte-native/components'
    import Item from '../store-item/StoreItem.svelte'

    let listOfItems = ['one', 'two', 'three']
    const goToStore = () => {
        navigate({page: Store})
    }

</script>
