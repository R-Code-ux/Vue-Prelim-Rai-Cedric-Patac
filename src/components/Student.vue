<template>
    <div class="p-2">
        <h1 class="font-bold text-2xl">Names of Student: </h1>
        <ul>
            <li v-for="stud in studInfo" :key="stud.name" :class="{ highlight: stud.score >= 90 }">{{ stud.name }}</li>
        </ul>

        <p>Passing Students: <span class="font-bold text-2xl">{{ passingStudents }}</span></p>
    </div>
</template>

<script setup>
import { computed, ref } from 'vue';

    //part 3
    const showList = ref(true);

    //part 2-4
    const studInfo = [
    { name: 'Raul', score: 99},
    { name: 'Vrai', score: 80},
    { name: 'James', score: 68},
    { name: 'Sonic', score: 70},
    { name: 'Jan', score: 90},
    ]

    //part 4
    const passingStudents = computed(() => {
        return studInfo.filter(student => student.score >= 70).length;
    })
</script>

<style scoped>
.highlight {
  color: green;
  font-weight: bold;
}
</style>