<template>

    <div class="flex flex-col items-center text-center mt-3 mx-2">
        <div class="w-10 h-10 mx-2 flex items-center justify-center border border-blue-500 rounded-full">
            <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                <path fill="#FE2712" d="M184 48l144 0c4.4 0 8 3.6 8 8l0 40L176 96l0-40c0-4.4 3.6-8 8-8zm-56 8l0 40L64 96C28.7 96 0 124.7 0 160l0 96 192 0 128 0 192 0 0-96c0-35.3-28.7-64-64-64l-64 0 0-40c0-30.9-25.1-56-56-56L184 0c-30.9 0-56 25.1-56 56zM512 288l-192 0 0 32c0 17.7-14.3 32-32 32l-64 0c-17.7 0-32-14.3-32-32l0-32L0 288 0 416c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-128z"/>
            </svg>
        </div>
        <h2 id="workExperiences" class="text-2xl font-bold text-blue-500 underline">
            Expériences professionnelles
        </h2>
    </div>
    

    <div v-for="workExperience in workExperiences" :key="workExperience.jobTitle" class="experience mx-4 mt-4">
        <h3 class="text-lg font-semibold text-blue-500">
            {{ workExperience.jobTitle }}
        </h3>
        <span class="text-sm font-semibold">
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
    </div>

</template>

<script setup>

    import { ref } from 'vue';

    const workExperiences = ref([
        {
            jobTitle: "Chargé de communication",
            company: "Mairie de Port-Bail-sur-Mer",
            startDate: "Janvier",
            endDate: "Décembre 2021",
            typeOfContract: "CDD",
            description: [
                "- Mise à jour du site internet",
                "- Gestion de projet"
            ]
        },
        {
            jobTitle: "Découverte du pôle digital",
            company: "Imprimerie HandiPrint",
            startDate: "Septembre",
            endDate: "Octobre 2020",
            typeOfContract: "Stage",
            description: [
                "- Web to Print",
                "- Impression à données variables"
            ]
        },
        {
            jobTitle: "Commercial en communication",
            company: "Agence Toile de Com",
            startDate: "Novembre",
            endDate: "Décembre 2018",
            typeOfContract: "Stage",
            description: [
                "- Relation commerciale",
                "- Phoning BtoB"
            ]
        },
        {
            jobTitle: "Chargé de communication institutionnelle",
            company: "Association Vire Avenir",
            startDate: "Novembre",
            endDate: "Décembre 2017",
            typeOfContract: "Stage",
            description: [
                "- Base de données intranet",
                "- Réalisation d'une étude"
            ]
        },
        {
            jobTitle: "Chargé de projet événementiel",
            company: "Auray Pays d'Artistes",
            startDate: "Mai",
            endDate: "Juillet 2017",
            typeOfContract: "Stage",
            description: [
                "- Organisation de visites guidées",
                "- Expérimentation en tant que guide"
            ]
        },
        {
            jobTitle: "Chargé de communication événementielle",
            company: "JS Cherbourg Handball",
            startDate: "Janvier 2017",
            endDate: "",
            typeOfContract: "Stage",
            description: [
                "- Rédaction web",
                "- Création de visuels pour panneaux LED"
            ]
        },
        {
            jobTitle: "Chargé de communication",
            company: "Galerie d'art Le Verrier",
            startDate: "Septembre 2016",
            endDate: "Mars 2017",
            typeOfContract: "Bénévolat",
            description: [
                "- Communication multicanale",
                "- Relations presse"
            ]
        }
    ])


</script>