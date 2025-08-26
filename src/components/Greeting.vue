<template>
    <!-- part5 -->
    <div class="p-4">
        <h2 class="text-4xl font-bold text-blue-700 ">Hello from Greeting Component</h2>
        <br>
        <h2 class="text-pink-500 font-bold">Hello, {{ capitalizeName }}</h2>
    </div>
</template>

<script setup>
    import { computed } from 'vue';
import { capitalize } from './util.js';

    //Part 7
    const props = defineProps({
        username: String
    })

    //Continuation of part 7
    const capitalizeName = computed(() => capitalize(props.username));
</script>