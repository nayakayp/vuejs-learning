<script>
export default {
    data(){
        return{
            show:true,
            numbers:[1,2,3,4]
        }
    }
}
</script>

<template>
    <div class="">
        <button @click="show=!show">Toggle List</button>
        <button @click="numbers.push(numbers.length+1)">Push Number</button>
        <button @click="numbers.pop()">Pop Number</button>
        <button @click="numbers.reverse()">Reverse Number</button>
        <ul v-if="show">
            <li v-for="number in numbers" :key="number">
                {{number}}
            </li>
        </ul>
        <p v-else>List hidden, please clik toggle list</p>
    </div>
</template>