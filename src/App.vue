<template>
    <Student />
    <Greeting :username="username"/>
</template>

<script setup>
import Greeting from './components/Greeting.vue';
import Student from './components/Student.vue';

    const username = "Spongebob Squarepants";

</script>