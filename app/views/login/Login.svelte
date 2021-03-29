<page {...pageProps}>
    <flexboxLayout {...flexboxLayoutProps}>
        <label horizontalAlignment="center" textWrap="true" verticalAlignment="middle">
            <formattedString>
                <span class="fas t-18" color="#63371E" text="Maco"/>
            </formattedString>
        </label>
        <image {...imageProps} tintColor="{leafTintColor}"></image>
        <PhoneTextField setCode={setCode} setPhone={setPhone}/>

        <button {...buttonProps}/>
    </flexboxLayout>
</page>

<script lang="typescript">
    import PhoneTextField from "./phoneNumberTextField/PhoneTextField.svelte"

    const pageProps: { [id: string]: string; } = {actionBarHidden: "true"}
    const flexboxLayoutProps = {
        backgroundColor: "#95C22B",
        flexDirection: "column", justifyContent: "space-around", alignItems: "center"
    }
    const buttonProps = {
        borderRadius: "5",
        backgroundColor: "#63371E",
        class: "my-button",
        color: "#A7D930",
        text: "Registrarme",
        height: 50,
        width: 300
    }
    const imageProps = {
        height: "80",
        src: "~/icons/seedling-solid.png",
    }

    let leafTintColor = "#507B00"
    let code: string = "+57"
    let phone: string = ""

    const setCode = (newCode) => {
        code = newCode
    }
    const setPhone = (newPhone) => {
        phone = newPhone
    }
</script>

<style>

    .fa_custom {
        color: #0099CC
    }

    .fas {
        font-family: "Font Awesome 5 Free", "fa-solid-900";
        font-weight: 2000;
    }

    .t-18 {
        font-size: 120;
    }
</style>

