<template>
    
    <div class="flex flex-col items-center text-center mt-3 mx-2">
        <div class="w-10 h-10 mx-2 flex items-center justify-center border border-green-500 rounded-full">
            <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
                <path fill="#10B981" d="M256 0l64 0c17.7 0 32 14.3 32 32l0 64c0 17.7-14.3 32-32 32l-64 0c-17.7 0-32-14.3-32-32l0-64c0-17.7 14.3-32 32-32zM64 64l128 0 0 48c0 26.5 21.5 48 48 48l96 0c26.5 0 48-21.5 48-48l0-48 128 0c35.3 0 64 28.7 64 64l0 320c0 35.3-28.7 64-64 64L64 512c-35.3 0-64-28.7-64-64L0 128C0 92.7 28.7 64 64 64zM176 437.3c0 5.9 4.8 10.7 10.7 10.7l202.7 0c5.9 0 10.7-4.8 10.7-10.7c0-29.5-23.9-53.3-53.3-53.3l-117.3 0c-29.5 0-53.3 23.9-53.3 53.3zM288 352a64 64 0 1 0 0-128 64 64 0 1 0 0 128z"/>
            </svg>
        </div>
        <h2 id="profile" class="text-2xl font-bold text-green-500 underline">
            Profil
        </h2>
    </div>

    
    <ul class="flex flex-col flex-wrap md:items-start justify-center flex-wrap">
        <li class="flex flex-col md:flex-row items-center justify-center mx-4 mt-4">
            <div class="w-10 h-10 flex items-center justify-center border border-green-500 rounded-none overflow-hidden">
                <svg class="w-6 h-6 animate-car" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">
                    <path fill="#10B981" d="M171.3 96L224 96l0 96-112.7 0 30.4-75.9C146.5 104 158.2 96 171.3 96zM272 192l0-96 81.2 0c9.7 0 18.9 4.4 25 12l67.2 84L272 192zm256.2 1L428.2 68c-18.2-22.8-45.8-36-75-36L171.3 32c-39.3 0-74.6 23.9-89.1 60.3L40.6 196.4C16.8 205.8 0 228.9 0 256L0 368c0 17.7 14.3 32 32 32l33.3 0c7.6 45.4 47.1 80 94.7 80s87.1-34.6 94.7-80l130.7 0c7.6 45.4 47.1 80 94.7 80s87.1-34.6 94.7-80l33.3 0c17.7 0 32-14.3 32-32l0-48c0-65.2-48.8-119-111.8-127zM434.7 368a48 48 0 1 1 90.5 32 48 48 0 1 1 -90.5-32zM160 336a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"/>
                </svg>
            </div>
            <span class="text-green-500 font-semibold flex flex-wrap text-center ml-2">
                Permis B avec véhicule personnel
            </span>
        </li>

        <li class="flex flex-col md:flex-row items-center justify-center mx-4 mt-4">
            <div class="w-10 h-10 flex items-center justify-center border border-green-500 rounded-none">
                <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <path fill="#10B981" d="M464 256A208 208 0 1 0 48 256a208 208 0 1 0 416 0zM0 256a256 256 0 1 1 512 0A256 256 0 1 1 0 256zm177.6 62.1C192.8 334.5 218.8 352 256 352s63.2-17.5 78.4-33.9c9-9.7 24.2-10.4 33.9-1.4s10.4 24.2 1.4 33.9c-22 23.8-60 49.4-113.6 49.4s-91.7-25.5-113.6-49.4c-9-9.7-8.4-24.9 1.4-33.9s24.9-8.4 33.9 1.4zM144.4 208a32 32 0 1 1 64 0 32 32 0 1 1 -64 0zm192-32a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"/>
                </svg>
            </div>
            <span class="text-green-500 font-semibold flex flex-wrap text-center ml-2">
                Relationnel - Organisé - Persévérant
            </span>
        </li>
    </ul>

</template>

<style scoped>

    @keyframes moveCar {
        0% {
            transform: translateX(-100%);
        }
        40% {
            transform: translateX(10%);
        }
        60% {
            transform: translateX(10%);
        }
        100% {
            transform: translateX(100%);
        }
    }

    .animate-car {
        animation: moveCar 2s ease-in-out infinite;
    }

</style>