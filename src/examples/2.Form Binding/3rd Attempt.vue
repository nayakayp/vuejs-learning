<script>
export default {
    data(){
        return {
            textInput:'Edit me',
            checked:false,
            multiCheckbox:[],
            picked:'One',
            selected:null,
            multiSelect:[]
        }
    }
}
</script>

<template>
    <div class="main">
        <div class="mb-4">
            <h2>Text Input</h2>
            <label for="">
                <input type="text" v-model="textInput">
                {{textInput}}
            </label>
        </div>
        <div class="mb-4">
            <h2>Checkbox</h2>
            <label for="checked">
                <input type="checkbox" id="checked" v-model="checked">
                Checked: {{checked}}
            </label>
        </div>
        <div class="mb-4">
            <h2>Multi Checkbox</h2>
            <label for="jack">
                <input value="Jack" id="jack" type="checkbox" v-model="multiCheckbox">
                Jack
            </label>
            <label for="john">
                <input value="John" id="john" type="checkbox" v-model="multiCheckbox">
                John
            </label>
            <label for="mike">
                <input value="Mike" id="mike" type="checkbox" v-model="multiCheckbox">
                Mike
            </label>
            <p>Checked names: {{multiCheckbox}}</p>
        </div>
        <div class="mb-4">
            <h2>Radio</h2>
            <label for="one">
                <input type="radio" value="One" id="one" v-model="picked">
                One
            </label>
            <label for="two">
                <input type="radio" value="Two" id="two" v-model="picked">
                Two
            </label>
            <p>Picked: {{picked}}</p>
        </div>
        <div class="mb-4">
            <h2>Select</h2>
            <select name="" id="" v-model="selected">
                <option value="Please select one" disabled>Please select one</option>
                <option value="A">A</option>
                <option value="B">B</option>
                <option value="C">C</option>
            </select>
            <p>Selected: {{selected}}</p>
        </div>
        <div class="mb-4">
            <h2>Multi Select</h2>
            <select name="" id="" v-model="multiSelect" multiple>
                <option value="A">A</option>
                <option value="B">B</option>
                <option value="C">C</option>
            </select>
            <p>Selected: {{multiSelect}}</p>
        </div>
    </div>
</template>