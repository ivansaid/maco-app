<bottomNavigation on:selectedIndexChanged={(item)=>{
    tabSelected(item)
}}>
    <tabStrip class="bottomTabStrip">
        <tabStripItem backgroundColor={firstTabColor} on:tap={()=>first()}>
            <label class="bottom-label" text="Home"/>
            <image src="~/icons/tree.png"/>
        </tabStripItem>
        <tabStripItem backgroundColor={secondTabColor} on:tap={()=>second()}>
            <label class="bottom-label" text="Buscar"/>
            <image src="~/icons/search.png"/>
        </tabStripItem>
        <tabStripItem backgroundColor={thirdTabColor} on:tap={()=>three()}>
            <label class="bottom-label" text="Cuenta"/>
            <image src="~/icons/person.png"/>
        </tabStripItem>
    </tabStrip>
    <tabContentItem>
        <CategoryLists addComponent={addComponentCategoryTab} props={props} selected={selected}/>
    </tabContentItem>
    <tabContentItem>
        <gridLayout>
            <Search addComponent={addComponentCategoryTab} props={props} selected={selected}/>
        </gridLayout>
    </tabContentItem>
    <tabContentItem>
        <gridLayout>
            <label class="h2 text-center" text="Account Page"/>
        </gridLayout>
    </tabContentItem>

</bottomNavigation>

<script>
    import CategoryLists from '../category-list/CategoryList.svelte'
    import Search from '../search/Search.svelte'

    let firstTabColor = "#EBA40F"
    let secondTabColor = "#748E1F"
    let thirdTabColor = "#748E1F"

    const first = () => {
        firstTabColor = "#EBA40F"
        secondTabColor = "#748E1F"
        thirdTabColor = "#748E1F"
    }
    const second = () => {
        firstTabColor = "#748E1F"
        secondTabColor = "#EBA40F"
        thirdTabColor = "#748E1F"
    }
    const three = () => {
        firstTabColor = "#748E1F"
        secondTabColor = "#748E1F"
        thirdTabColor = "#EBA40F"
    }

    export let selected
    export let props
    export let visibility
    export let addComponentCategoryTab
    export let tabSelected
</script>
