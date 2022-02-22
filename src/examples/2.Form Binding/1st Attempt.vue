<script>
export default {
    data(){
            return{
            textInput:'Edit me',
            checked: false,
            checkedNames:["Yoga"],
            picked:null,
            selected:'',
            multiSelected:[]
        }
    }
}
</script>

<template>
    <div class="">
        <div class="">
            <h2 class="text-2xl font-bold">Text Input</h2>
            <input class="border p-2" type="text" v-model="textInput"> <span>{{textInput}}</span>
        </div>
        <div class="mt-4">
            <h2 class="text-2xl font-bold">Checkbox</h2>
            <label for="checkbox">
                <input v-model="checked" id="checkbox" type="checkbox">
                Checked: {{checked}}
            </label>
        </div>
        <div class="mt-4">
            <h2 class="text-2xl font-bold">Multi Checkbox</h2>
            <div class="flex space-x-2">
                <label for="nayaka">
                <input value="Nayaka" v-model="checkedNames" id="nayaka" type="checkbox">
                Nayaka
                </label>
                <label for="yoga">
                    <input value="Yoga" v-model="checkedNames" id="yoga" type="checkbox">
                    Yoga
                </label>
                <label for="pradipta">
                    <input value="Pradipta" v-model="checkedNames" id="pradipta" type="checkbox">
                    Pradipta
                </label>
            </div>
            <ul class="list-decimal mt-1">
                <p class="italic">Checked names:</p>
                <li class="ml-4" v-for="name in checkedNames" :key="name">
                    {{name}}
                </li>
            </ul>
        </div>
        <div class="mt-4">
            <h2 class="text-2xl font-bold">Radio</h2>
            <div class="">
                <label for="one">
                    <input id="one" type="radio" value="One" v-model="picked">
                    One
                </label>
                <label for="two">
                    <input id="two" type="radio" value="Two" v-model="picked">
                    Two
                </label>
            </div>
            <p class="mt-1">Picked: {{picked}}</p>
        </div>
        <div class="mt-4">
            <h2 class="text-2xl font-bold">Select</h2>
            <div class="">
                <select v-model="selected" class="border w-full">
                    <option value="Please select one" disabled>Please select one</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                </select>
            </div>
            <p class="mt-1">Selected: {{selected}}</p>
        </div>
        <div class="mt-4">
            <h2 class="text-2xl font-bold">Multi Select</h2>
            <div class="">
                <select v-model="multiSelected" class="border w-full" multiple>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                </select>
            </div>
            <p class="mt-1">Selected: {{multiSelected}}</p>
        </div>
    </div>
</template>