<stackLayout>
    <flexboxLayout {...flexboxLayoutProps}>
        <gridLayout columns="180, 150" rows="50">
            <label horizontalAlignment="center" textWrap="true" verticalAlignment="middle">
                <formattedString>
                    <span {...enterTextProps}/>
                </formattedString>
            </label>
        </gridLayout>
    </flexboxLayout>
    <flexboxLayout {...flexboxLayoutProps}>
        <gridLayout columns="120, 210" rows="100">
            <listPicker {...listPickerProps} class="picker" on:selectedIndexChange={(val)=>{
                setCode(val["value"])}}/>
            <textField {...textFieldProps} class="textField" on:textChange={(val)=>{
                setPhone(val["value"])
            }}></textField>

        </gridLayout>
    </flexboxLayout>
</stackLayout>

<script>
    import countryCodeList from "../CountryCodes.ts"
    import {action} from '@nativescript/core/ui/dialogs'

    export let setPhone;
    export let setCode;

    //components props
    const textFieldProps = {col: "1", row: "0", text: "", hint: "...", keyboardType: "phone"}
    const listPickerProps = {
        col: "0", row: "0",
        items: countryCodeList.map(codeItem => {
            return codeItem["name"]
        }),
    }
    const enterTextProps = {style: "color: black", class: "fas t-18", text: "Ingresa tu numero de telefono: "}
    const flexboxLayoutProps = {alignItems: "center", justifyContent: "space-around"}
</script>

<style>
    .picker {
        background-color: #63371E;
        color: #A7D930;
        border-radius: 5;
        width: 200;
        height: 50;
        vertical-align: baseline;
    }

    .textField {
        justify-content: "center";
        background-color: #63371E;
        color: #95C22B;
        border-radius: 5;
        width: 200;
        height: 50;
        vertical-align: baseline;
    }

    .fas {
        font-family: "Font Awesome 5 Free", "fa-solid-900";
        font-weight: 200;
    }

    .t-18 {
        font-size: 20;
    }
</style>
