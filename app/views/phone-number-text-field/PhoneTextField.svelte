<stackLayout class="info-stack">
    <label class="enter-text-label" textWrap="true" verticalAlignment="middle">
        <formattedString>
            <span class="enterText"/>
        </formattedString>
    </label>
    <stackLayout class="number-field" orientation="horizontal">
        <listPicker {...listPickerProps} class="picker" on:selectedIndexChange={(val)=>{
                setCode(val["value"])}}/>
        <textField class="textField" on:textChange={(val)=>{
                setPhone(val["value"])
            }}></textField>
    </stackLayout>
</stackLayout>

<script>
    import countryCodeList from "../login/CountryCodes.ts"

    export let setPhone;
    export let setCode;
    let codes = countryCodeList.map(codeItem => {
        return codeItem["dial_code"]
    }).sort((a, b) => {
        a = parseInt(a.slice(1))
        b = parseInt(b.slice(1))
        if (parseInt(a) < b) {
            return -1
        }
        if (a > b) {
            return 1
        }
        return 0
    })
    codes.splice(0, 0, "+57")
    //components props
    const listPickerProps = {
        items: codes,
    }
</script>

