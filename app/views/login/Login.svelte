<page class="loginPage">
    <flexboxLayout class="flexboxLayoutLogin">
        <label class="titleLabel">
            <formattedString>
                <span class="mainTitle"/>
            </formattedString>
        </label>
        <image class="leafImage" src="~/icons/seedling-solid.png"></image>
        <PhoneTextField setCode={setCode} setPhone={setPhone}/>
        <button class="registerButton" on:tap={()=>goToStores()}/>
    </flexboxLayout>
</page>

<script>
    import PhoneTextField from "../phone-number-text-field/PhoneTextField.svelte"
    import Stores from "../main/Main.svelte"
    import {navigate} from 'svelte-native'

    let code = "+57"
    let phone = ""

    const setCode = (newCode) => {
        code = newCode
    }
    const setPhone = (newPhone) => {
        phone = newPhone
    }
    const goToStores = () => {
        navigate({page: Stores})
    }
</script>

