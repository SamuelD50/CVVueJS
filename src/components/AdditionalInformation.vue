<template>
    
    <div class="my-2 mb-20">
        <h2 id="additionalInformation" class="text-2xl font-bold text-white my-2 mx-2 text-center">
            Informations complémentaires
        </h2>
        
        <ul class="flex flex-col items-center gap-1 text-white mx-2">
            <li v-for="additional in additionnals" :key="additional" class="text-white">
                {{ additional }}
            </li>
        </ul>
    </div>
    
</template>

<script setup>
    const additionnals = [
        "Permis B + véhicule personnel"
    ]
</script>