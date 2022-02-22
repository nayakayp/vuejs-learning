<script>
export default {
    data(){
        return{
            show:true,
            numbers:[1,2,3]
        }
    },
    methods:{
        toggleList(){
            this.show=!this.show
        },
        pushNumber(){
            this.numbers.push(this.numbers.length+1)
        },
        popNumber(){
            this.numbers.pop()
        },
        reverseList(){
            this.numbers.reverse()
        }
    }
}
</script>

<template>
    <div class="">
        <button @click="toggleList">Toggle List</button>
        <button @click="pushNumber">Push Number</button>
        <button @click="popNumber">Pop Number</button>
        <button @click="reverseList">Reverse List</button>

        <ul v-if="show">
            <li v-for="number in numbers" :key="number">
                {{ number }}
            </li>
        </ul>
        <p v-else-if="!show">List is hidden</p>
    </div>
</template>