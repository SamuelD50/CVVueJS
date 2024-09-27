<template>

    <div class="flex flex-col items-center text-center mt-3 mx-2 py-3 bg-blue-300">
        <div class="w-10 h-10 mx-2 flex items-center justify-center border border-blue-800 rounded-full">
            <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">
                <path fill="#2F4F7F" d="M274.9 34.3c-28.1-28.1-73.7-28.1-101.8 0L34.3 173.1c-28.1 28.1-28.1 73.7 0 101.8L173.1 413.7c28.1 28.1 73.7 28.1 101.8 0L413.7 274.9c28.1-28.1 28.1-73.7 0-101.8L274.9 34.3zM200 224a24 24 0 1 1 48 0 24 24 0 1 1 -48 0zM96 200a24 24 0 1 1 0 48 24 24 0 1 1 0-48zM224 376a24 24 0 1 1 0-48 24 24 0 1 1 0 48zM352 200a24 24 0 1 1 0 48 24 24 0 1 1 0-48zM224 120a24 24 0 1 1 0-48 24 24 0 1 1 0 48zm96 328c0 35.3 28.7 64 64 64l192 0c35.3 0 64-28.7 64-64l0-192c0-35.3-28.7-64-64-64l-114.3 0c11.6 36 3.1 77-25.4 105.5L320 413.8l0 34.2zM480 328a24 24 0 1 1 0 48 24 24 0 1 1 0-48z"/>
            </svg>
        </div>
        <h2 id="interests" class="text-2xl font-bold text-blue-800 underline">
            Intérêts
        </h2>
    </div>

  

    <div v-for="interest in interests" :key="interest.theme" class="degree pl-3 mt-2 bg-[#F5F5F5]">
        <h3 class="text-lg font-semibold text-blue-500">
            {{ interest.theme }}
        </h3>
    </div>

</template>

<script setup>

    import { ref } from 'vue';

    const interests = ref([
        {
            theme: "Beaux-Arts"
        },
        {
            theme: "Multimédia et numérique"
        },
        {
            theme: "Course à pied"
        },
        {
            theme: "Culture générale"
        }
    ])


</script>