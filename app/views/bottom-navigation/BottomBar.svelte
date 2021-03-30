<bottomNavigation>
    <tabStrip class="bottomTabStrip">
        <tabStripItem>
            <label class="bottom-label" text="Home"/>
            <image src="~/icons/tree-solid.png"/>
        </tabStripItem>
        <tabStripItem>
            <label class="bottom-label" text="Buscar"/>
            <image src="~/icons/search-solid.png"/>
        </tabStripItem>
        <tabStripItem>
            <label class="bottom-label" text="Cuenta"/>
            <image src="~/icons/user-solid.png"/>
        </tabStripItem>
    </tabStrip>

    <tabContentItem>
        <Stores/>
    </tabContentItem>
    <tabContentItem>
        <gridLayout>
            <label class="h2 text-center" text="Search Page"/>
        </gridLayout>
    </tabContentItem>
    <tabContentItem>
        <gridLayout>
            <label class="h2 text-center" text="Account Page"/>
        </gridLayout>
    </tabContentItem>

</bottomNavigation>

<script>
    import Stores from '../stores-list/StoresList.svelte'
</script>
