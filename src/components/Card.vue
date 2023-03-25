<template>
    <div class="flex justify-center items-center w-5/6 flex-col gap-4 p-5 rounded-xl bg-Dark-Grayish-Blue max-w-lg">
        <h1 class="text-Neon-Green">Advice #{{ id }}</h1>
        <p class="text-Light-Cyan text-2.5xl text-center">"{{ advice }}"</p>
        <img src="../assets/images/pattern-divider-mobile.svg" class="w-full" alt="">
        <button class="bg-Neon-Green p-3 rounded-full" @click="fetchAdvice" >
            <img
                src="../assets/images/icon-dice.svg"
                alt="dice icon"
            >
            
        </button>
    </div>
</template>
<script setup>

    import { ref, onMounted } from "vue";
    import axios from 'axios';

    const advice = ref(null);
    const id = ref(null)
    const i = ref(1)
    const fetchAdvice = () => {
        axios
        .get("https://api.adviceslip.com/advice")
        .then(response => {
        advice.value = response.data.slip.advice;
        id.value = response.data.slip.id;
        console.log(advice.value)
        })
        .catch(error => {
        console.error(error);
        });
    };

    onMounted(fetchAdvice);

</script>
<style>

    button{
        transition: 0.3s;
    }   
    button:hover {
        box-shadow: 0 0 15px 3px hsl(150, 100%, 66%);
    }
</style>