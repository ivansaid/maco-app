<absolute-layout class="x" margin="10">
    <textView editable="{false}" fontSize="20" heigth="10" on:tap={()=>{goTo()}} width="120">
        <formattedString>
            <span text={number}/>
        </formattedString>
    </textView>
</absolute-layout>


<script>
    import {navigate} from "svelte-native"
    import Store from "../store/Store.svelte"

    export let number
    export let changeComponent

    const goTo = () => {
        changeComponent("store", {props: {comingFrom: number, changeComponent: changeComponent}})
    }

</script>

<style>
    .x {
        border-radius: 20;
        border-color: #EBA40F;
        border-width: 3;
    }
</style>
