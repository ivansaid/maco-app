<stackLayout>
    <flexboxLayout {...flexboxLayoutProps2}>
        <gridLayout backgroundColor="white" columns="330" rows="30">
            <label horizontalAlignment="center" textWrap="true" verticalAlignment="middle">
                <formattedString>
                    <span class="enterText"/>
                </formattedString>
            </label>
        </gridLayout>
    </flexboxLayout>
    <flexboxLayout {...flexboxLayoutProps}>
        <gridLayout columns="150,30, 150" rows="140">
            <listPicker {...listPickerProps} class="picker" on:selectedIndexChange={(val)=>{
                setCode(val["value"])}}/>
            <textField class="textField" on:textChange={(val)=>{
                setPhone(val["value"])
            }}></textField>

        </gridLayout>
    </flexboxLayout>
</stackLayout>

<script>
    import countryCodeList from "../login/CountryCodes.ts"

    export let setPhone;
    export let setCode;

    //components props
    const listPickerProps = {
        col: "0", row: "0",
        items: countryCodeList.map(codeItem => {
            return codeItem["name"]
        }),
    }
    const flexboxLayoutProps2 = {alignItems: "start-flex", justifyContent: "space-around"}
    const flexboxLayoutProps = {alignItems: "center", justifyContent: "space-around"}
</script>

