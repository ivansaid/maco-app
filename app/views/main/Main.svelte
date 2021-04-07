<page>
    <ActionBar removeComponents={removeComponents} visibility={visibility[visibility.length-1]}/>
    <BottomBar addComponentCategoryTab={addComponentCategoryTab} props={props} selected={selected}
               tabSelected={tabSelected} visibility={visibility}/>
</page>

<script>
    import ActionBar from '../upper-bar/ActionBar.svelte'
    import BottomBar from '../bottom-navigation/BottomBar.svelte'
    import Store from "../store/Store.svelte";
    import List from "../list/List.svelte";
    import SearchExample from '../search/SearchExample.svelte'
    import * as application from "@nativescript/core/application"
    import {AndroidApplication, AndroidActivityBackPressedEventData} from "@nativescript/core/application"

    let selected = [List]
    let visibility = ["hidden"]
    let props = [{}]
    let index

    application.android.on(AndroidApplication.activityBackPressedEvent, (data = AndroidActivityBackPressedEventData) => {
        data.cancel = true
        removeComponents()
    });


    const addComponentCategoryTab = (component, componentProps) => {
        switch (component) {
            case "store":
                selected = selected.concat(Store)
                props = props.concat(componentProps)
                visibility = visibility.concat("visible")
        }
    }

    const tabSelected = (item) => {
        index = item.newIndex
        if (index === 0) {
            selected = [List]
            visibility = ["hidden"]
            props = [{}]

        } else if (index === 1) {
            selected = [SearchExample]
            visibility = ["hidden"]
            props = [{}]
        }
    }

    const removeComponents = () => {
        if (selected.length > 1) {
            let temp1 = [...selected]
            let temp2 = [...props]
            let temp3 = [...visibility]
            temp1.pop()
            temp2.pop()
            temp3.pop()
            selected = temp1
            props = temp2
            visibility = temp3
        }
    }

</script>
