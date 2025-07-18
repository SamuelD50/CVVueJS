<template>

    <div class="my-5">
        <h2 id="workExperiences" class="text-2xl font-bold text-blue-800 my-2">
            Expériences professionnelles
        </h2>
        
        <div v-for="workExperience in workExperiences" :key="workExperience.jobTitle">
            <h3 class="text-lg font-semibold text-blue-800">
                {{ workExperience.jobTitle }}
            </h3>
            <span class="text-sm text-black font-semibold">
                {{ workExperience.company }} | {{ workExperience.startDate }} 
                <template v-if="workExperience.endDate">
                    - {{ workExperience.endDate }}
                </template>
                | {{ workExperience.typeOfContract }}
            </span>

            <ul>
                <li v-if="workExperience.description.length >= 2" class="text-md">
                    {{ workExperience.description[0] }} & {{ workExperience.description[1] }}
                </li>
            </ul>
        </div>
    </div>

</template>

<script setup>

    const workExperiences = [
        {
            jobTitle: "Développeur d'application mobile",
            company: "ASAM de Cherbourg",
            startDate: "Octobre 2024",
            endDate: "Juin 2025",
            typeOfContract: "Service civique",
            description: [
                "Création d'une application mobile",
                "GitHub Actions"
            ]
        },
        {
            jobTitle: "Chargé de communication",
            company: "Mairie de Port-Bail-sur-Mer",
            startDate: "Janvier",
            endDate: "Décembre 2021",
            typeOfContract: "CDD",
            description: [
                "Mise à jour du site internet",
                "Gestion de projet"
            ]
        },
        {
            jobTitle: "Découverte du pôle digital",
            company: "Imprimerie HandiPrint",
            startDate: "Septembre",
            endDate: "Octobre 2020",
            typeOfContract: "Stage",
            description: [
                "Web to Print",
                "Impression à données variables"
            ]
        },
        {
            jobTitle: "Commercial en communication",
            company: "Agence Toile de Com",
            startDate: "Novembre",
            endDate: "Décembre 2018",
            typeOfContract: "Stage",
            description: [
                "Relation commerciale",
                "Phoning BtoB"
            ]
        },
        {
            jobTitle: "Chargé de communication institutionnelle",
            company: "Association Vire Avenir",
            startDate: "Novembre",
            endDate: "Décembre 2017",
            typeOfContract: "Stage",
            description: [
                "Base de données intranet",
                "Réalisation d'une étude"
            ]
        },
        {
            jobTitle: "Chargé de projet événementiel",
            company: "Auray Pays d'Artistes",
            startDate: "Mai",
            endDate: "Juillet 2017",
            typeOfContract: "Stage",
            description: [
                "Organisation",
                "Expérimentation de visites guidées"
            ]
        },
        {
            jobTitle: "Chargé de communication événementielle",
            company: "JS Cherbourg Handball",
            startDate: "Janvier 2017",
            endDate: "",
            typeOfContract: "Stage",
            description: [
                "Rédaction web",
                "Création de visuels pour panneaux LED"
            ]
        },
        {
            jobTitle: "Chargé de communication",
            company: "Galerie d'art Le Verrier",
            startDate: "Septembre 2016",
            endDate: "Mars 2017",
            typeOfContract: "Bénévolat",
            description: [
                "Communication multicanale",
                "Relations presse"
            ]
        }
    ]
</script>