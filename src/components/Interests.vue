<template>
    
    <div class="py-2">
        <h2 id="interests" class="text-2xl font-bold text-white my-2 mx-2 text-center">
            Intérêts
        </h2>
        <ul class="flex flex-col items-center gap-1 text-white mx-2">
            <li v-for="interest in interests" :key="interests" class="text-white">
                {{ interest }}
            </li>
        </ul>
    </div>

</template>

<script setup>

    const interests = [
        "Beaux-Arts",
        "Multimédia et numérique",
        "Course à pied",
        "Culture générale",
    ]


</script>