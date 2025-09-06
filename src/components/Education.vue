<template>

    <div class="my-2">
        <h2 id="education" class="text-2xl font-bold text-blue-800 my-1">
            Formation
        </h2>

        <div v-for="degree in degrees" :key="degree.degreeTitle">
            <h3 class="text-lg font-semibold text-blue-800">
                {{ degree.degreeTitle }}
            </h3>
            <span class="text-sm text-black font-semibold">
                {{ degree.school }} |
                <template v-if="degree.location">
                    {{ degree.location }} |
                </template>
                <template v-if="degree.startDate">
                {{ degree.startDate }} -
                </template>
                <template v-if="degree.endDate">
                    {{ degree.endDate}}
                </template>
            </span>
        </div>
    </div>

</template>

<script setup>

    const degrees = [
        {
            degreeTitle: "Bac + 2 Développeur intégrateur web",
            school: "OpenClassrooms & GRETA",
            startDate: "Mai 2023",
            endDate: "Avril 2024"
        },
        {
            degreeTitle: "Initiation au logiciel InDesign",
            school: "GRETA",
            location: "Cherbourg-en-Cotentin",
            startDate: "",
            endDate: "Novembre 2021"
        },
        /* {
            degreeTitle: "Excel niveau 1",
            school: "CNFPT",
            location: "Port-Bail-sur-Mer",
            startDate: "",
            endDate: "Août 2021"
        },
        {
            degreeTitle: "Fondamentaux du marketing numérique",
            school: "Google Ateliers Numériques",
            startDate: "",
            endDate: "Juin 2020"
        }, */
        {
            degreeTitle: "BTS Communication",
            school: "Lycée Pierre et Marie Curie",
            location: "Saint-Lô",
            startDate: "2016",
            endDate: "2019"
        },
        {
            degreeTitle: "Baccalauréat littéraire",
            school: "Lycée Victor Grignard",
            location: "Cherbourg-en-Cotentin",
            startDate: "",
            endDate: "2016"
        }
    ]
</script>