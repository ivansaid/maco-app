<page backgroundColor="#748E1F" class="login-page">
    <stacklayout class="main-layout-login" margin="10">
        <image class="login-icon" height="40%" src="~/icons/maco_with_name.png" stretch="aspectFit"
               width="70%"></image>
        <PhoneTextField setCode={setCode} setPhone={setPhone}/>
        <button class="register-button" on:tap={()=>goToStores()}/>
    </stacklayout>
</page>

<script>

    import PhoneTextField from "../phone-number-text-field/PhoneTextField.svelte"
    import Stores from "../main/Main.svelte"
    import {navigate} from "svelte-native";
    import {onMount} from "svelte"
    import * as application from "@nativescript/core/application"


    export let isStart = false
    let code = "+57"
    let phone = ""

    if (application.android) {
        application.android.on(application.AndroidApplication.activityBackPressedEvent, () => {
            application.exitEvent
        });
    }


    const setCode = (newCode) => {

        code = newCode
    }
    const setPhone = (newPhone) => {
        phone = newPhone
    }
    onMount(() => {
        console.log(application.exitEvent)
    })

    const goToStores = () => {
        navigate({page: Stores})
    }

</script>

