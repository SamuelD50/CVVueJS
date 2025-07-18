<template>

    <div class="my-2">
        <h2 id="skills" class="text-2xl font-bold text-white my-2 mx-2 text-center">
            Compétences techniques
        </h2>

        <ul class="flex flex-wrap justify-start mx-2">
            <li v-for="skill in skills" :key="skill" class="text-white w-1/2 text-center">
                {{ skill }}
            </li>
        </ul>
    </div>
    
</template>

<script setup>

    const skills = [
        "HTML/CSS",
        "JavaScript",
        "ReactJS",
        "NodeJS",
        "ExpressJS",
        "MongoDB",
        "VueJS",
        "TailwindCSS",
        "Flutter",
        "Firebase",
    ]

</script>