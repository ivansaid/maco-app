<stackLayout>
    <label color="Black">Vivero {props.itemProps}</label>
    <listView backgroundColor="gray" items="{listOfItems}">
        <Template let:item>
            <label text="{item}"/>
        </Template>
    </listView>
</stackLayout>
<script>
    import {Template} from 'svelte-native/components'
    import {onMount} from 'svelte'

    export let props


    let listOfItems = ["Plant 1", "Plant 2", "Plant 3", "Plant 4", "Plant 5", "Plant 6", "Plant 7",
        "Plant 8", "Plant 9", "Plant 10", "Plant 11", "Plant 12", "Plant 13", "Plant 14", "Plant 15", "Plant 16",
        "Plant 17", "Plant 18", "Plant 19"]

</script>
