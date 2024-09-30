<template>

    <div class="flex flex-col items-center text-center mt-3 mx-2">
        <div class="w-10 h-10 mx-2 flex items-center justify-center border border-green-500 rounded-full">
            <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                <path fill="#10B981" d="M495.9 166.6c3.2 8.7 .5 18.4-6.4 24.6l-43.3 39.4c1.1 8.3 1.7 16.8 1.7 25.4s-.6 17.1-1.7 25.4l43.3 39.4c6.9 6.2 9.6 15.9 6.4 24.6c-4.4 11.9-9.7 23.3-15.8 34.3l-4.7 8.1c-6.6 11-14 21.4-22.1 31.2c-5.9 7.2-15.7 9.6-24.5 6.8l-55.7-17.7c-13.4 10.3-28.2 18.9-44 25.4l-12.5 57.1c-2 9.1-9 16.3-18.2 17.8c-13.8 2.3-28 3.5-42.5 3.5s-28.7-1.2-42.5-3.5c-9.2-1.5-16.2-8.7-18.2-17.8l-12.5-57.1c-15.8-6.5-30.6-15.1-44-25.4L83.1 425.9c-8.8 2.8-18.6 .3-24.5-6.8c-8.1-9.8-15.5-20.2-22.1-31.2l-4.7-8.1c-6.1-11-11.4-22.4-15.8-34.3c-3.2-8.7-.5-18.4 6.4-24.6l43.3-39.4C64.6 273.1 64 264.6 64 256s.6-17.1 1.7-25.4L22.4 191.2c-6.9-6.2-9.6-15.9-6.4-24.6c4.4-11.9 9.7-23.3 15.8-34.3l4.7-8.1c6.6-11 14-21.4 22.1-31.2c5.9-7.2 15.7-9.6 24.5-6.8l55.7 17.7c13.4-10.3 28.2-18.9 44-25.4l12.5-57.1c2-9.1 9-16.3 18.2-17.8C227.3 1.2 241.5 0 256 0s28.7 1.2 42.5 3.5c9.2 1.5 16.2 8.7 18.2 17.8l12.5 57.1c15.8 6.5 30.6 15.1 44 25.4l55.7-17.7c8.8-2.8 18.6-.3 24.5 6.8c8.1 9.8 15.5 20.2 22.1 31.2l4.7 8.1c6.1 11 11.4 22.4 15.8 34.3zM256 336a80 80 0 1 0 0-160 80 80 0 1 0 0 160z"/>
            </svg>
        </div>
        <h2 id="skills" class="text-2xl font-bold text-green-500 underline">
            Compétences
        </h2>
    </div>

    
    <div v-for="skill in skills" :key="skill.skillTitle" class="skill mx-4 mt-4">
        <h3 class="text-lg font-semibold text-green-500">
            {{ skill.skillTitle }}
        </h3>
        <ul v-if="skill.description" class="text-sm font-semibold" :class="{'grid grid-cols-2': skill.skillTitle === 'Technique'}">
            <li v-for="(ability, index) in skill.description" :key="index">
                {{ ability }}
            </li>
        </ul>
    </div>
    
    <!-- <div v-for="workExperience in workExperiences" :key="workExperience.jobTitle" class="experience mx-4 mt-4">
        <h3 class="text-lg font-semibold text-blue-500">
            {{ workExperience.jobTitle }}
        </h3>
        <span class="text-xs font-semibold">
            {{ workExperience.company }} | {{ workExperience.startDate }} 
            <template v-if="workExperience.endDate">
                - {{ workExperience.endDate }}
            </template>
            | {{ workExperience.typeOfContract }}
        </span>

        <ul>
            <li v-for="(task, index) in workExperience.description" :key="index" class="text-md">
                {{ task }}
            </li>
        </ul>
    </div> -->
</template>

<script setup>

    import { ref } from 'vue';

    const skills = ref([
        {
            skillTitle: "Langues",
            description: [
                "Anglais et espagnol: lu, écrit et parlé"
            ]
        },
        {
            skillTitle: "Bureautique",
            description: [
                "Pack Office (Word, Excel, PowerPoint)"
            ]
        },
        {
            skillTitle: "Technique",
            description: [
                "HTML/CSS",
                "JavaScript",
                "ReactJS",
                "NodeJS",
                "ExpressJS",
                "MongoDB",
                "VueJS",
                "TailwindCSS",
                "Swift",
                "Java",
                "Kotlin"
            ]
        }
    ])


</script>