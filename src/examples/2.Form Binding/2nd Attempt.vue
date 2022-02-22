<script>
export default {
    data(){
        return{
            textInput:'Edit me',
            isChecked:false,
            multiCheckbox:[],
            picked:'none',
            selected:null,
            multiSelected:[]
        }
    }
}
</script>

<template>
    <div id="main">
        <div class="mb-4">
            <h2 class="text-2xl font-bold">Text Input</h2>
            <label for="textInput">
                <input type="text" id="textInput" v-model="textInput" class="border">
                {{textInput}}
            </label>
        </div>
        <div class="mb-4">
            <h2 class="text-2xl font-bold">Checkbox</h2>
            <label for="checkbox">
                <input type="checkbox" id="checkbox" v-model="isChecked" class="border">
                Checked: {{isChecked}}
            </label>
        </div>
        <div class="mb-4">
            <h2 class="text-2xl font-bold">Multi Checkbox</h2>
            <div class="flex space-x-2">
                <label for="jack">
                    <input type="checkbox" value="Jack" id="jack" v-model="multiCheckbox">
                    Jack
                </label>
                <label for="john">
                    <input type="checkbox" value="John" id="john" v-model="multiCheckbox">
                    John
                </label>
                <label for="mike">
                    <input type="checkbox" value="Mike" id="mike" v-model="multiCheckbox">
                    Mike
                </label>
            </div>
            <p>Checked names: {{multiCheckbox}}</p>
        </div>
        <div class="mb-4">
            <h2 class="text-2xl font-bold">Radio</h2>
            <div class="">
                <label for="one">
                    <input type="radio" value="One" id="one" v-model="picked" class="border">
                    One
                </label>
                <label for="two">
                    <input type="radio" value="Two" id="two" v-model="picked" class="border">
                    Two
                </label>
            </div>
            <p>Picked: {{picked}}</p>
        </div>
        <div class="mb-4">
            <h2 class="text-2xl font-bold">Select</h2>
            <div class="">
                <select name="" id="" v-model="selected">
                    <option value="Please select" disabled>Please select</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                </select>
            </div>
            <p>Selected: {{selected}}</p>
        </div>
        <div class="mb-4">
            <h2 class="text-2xl font-bold">Multi Select</h2>
            <div class="">
                <select name="" id="" v-model="multiSelected" multiple>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                </select>
            </div>
            <p>Selected: {{multiSelected}}</p>
        </div>
    </div>
</template>