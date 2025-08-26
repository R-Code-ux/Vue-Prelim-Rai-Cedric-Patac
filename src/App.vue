<template>
    <Student />
    <Greeting :username="username"/>
</template>

<script setup>
// create a Vue project, install Node.js first. Then install
//  Vue CLI with npm install -g @vue/cli. Create a project using 
// vue create my-vue-app, go into the folder (cd my-vue-app), and run it with npm run
//  serve. Open your browser at http://localhost:8080 to see your app.

import Greeting from './components/Greeting.vue';
import Student from './components/Student.vue';

    const username = "Spongebob Squarepants";

</script>