<script>
export default {
    data(){
        return{
            show:false,
            numbers:[1,2,3,4,5]
        }
    }
}
</script>

<template>
    <div class="root">
        <button @click="show=!show">Toggle List</button>
        <button @click="numbers.push(numbers.length + 1)">Push List</button>
        <button @click="numbers.pop()">Pop List</button>
        <button @click="numbers.reverse()">Reverse List</button>
        <ul v-if="show">
            <li v-for="number in numbers" :key="number">
                {{number}}
            </li>
        </ul>
        <p v-else-if="!show">List disembunyikan. Klik Toggle List</p>
    </div>
</template>