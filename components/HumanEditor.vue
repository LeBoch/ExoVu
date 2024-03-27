<template>
    <!-- <div id="range" class="demo">
        <div v-for="n in props.userLength">  
            <input type="text" v-model="name" class="Name">
            <input type="text" v-model="firstName" class="FirstName">
            <input type="Number" v-model="age" class="Age"> 
            <button @click="envoyer()"> Envoyer </button>
            {{  n }}
        </div>
    </div> -->

    <div id="range" class="demo">
    <input type="text" v-model="promptName" :placeholder="promptName" class="Name">
    <input type="text" v-model="promptFirstName" :placeholder="promptFirstName" class="FirstName">
    <input type="Number" v-model="pomptAge" :placeholder="promptAge" class="Age"> 
    <button @click="send()"> Modifer </button>
</div>

</template>


<script setup>
import {defineProps , defineEmits , ref} from "vue"
const props = defineProps(['name', 'firstName' , 'age' ])
const emit = defineEmits(['emitName'] , ['emitFirstName'], ['emitAge'])
const promptName = ref(props.name)
const promptFirstName = ref(props.firstName)
const promptAge = ref(props.age)


function send() {
    // if(!promptName.value || !promptName.value || !promptAge.value ) {
    //     error.value = true
    // }else{
    //     open.value = false
    //     error.value = false

        emit('emitName' , promptName.value)
        emit('emitFirstName' , promptFirstName.value)
        emit('emitAge' , promptAge.value)

    }
    // !user.value ? (error.value = true) : (open.value = false , error.value = false , emit('send' , user.value ) );
// }
// const emit = defineEmits(['close'])
// const name = ref('')
// const firstName = ref('')
// const age = ref('')


// function envoyer() {
    
// }
</script>
