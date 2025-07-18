<template>
    <div class="my-2">
        <h2 id="contact" class="text-2xl font-bold text-white my-2 mx-2 text-center">
            Contact
        </h2>

        <ul class="flex flex-col items-center gap-1 text-white mx-2">
            <li class="flex flex-row gap-1">
                <span>
                    Téléphone : 
                </span>
                <a :href="`tel:${contact.phone}`">
                    06 42 90 63 53
                </a>
            </li>

            <li class="flex flex-row gap-1">
                <span>
                    Mail :
                </span>
                <a :href="`mailto:${contact.email}`">
                    {{ contact.email }}
                </a>
            </li>

            <li class="text-white text-center">
                <div class="flex flex-col items-center">
                    <div class="flex items-baseline gap-1">
                        <span>
                            Adresse :
                        </span>
                        <span>
                            {{ contact.address[0] }}
                        </span>
                    </div>
                    <ul>
                        <li v-for="(line, index) in contact.address.slice(1)" :key="index">
                            {{ line }}
                        </li>
                    </ul>
                </div>
            </li>
        </ul>
    </div>
    
</template>

<script setup>

    const contact = {
        phone: "+33 6 42 90 63 53",
        email: "duflos.samuel@gmail.com",
        address: 
        [
            "1 impasse Lizinska de Mirbel",
            "Appartement C15",
            "50130 CHERBOURG-EN-COTENTIN"
        ],
    }

</script>