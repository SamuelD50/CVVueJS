<template>

    <nav class="flex items-center w-full flex-wrap bg-teal p-6">
        <div class="flex flex-col sm:flex-row flex-wrap items-center justify-between text-white w-full">
            <div class="flex items-center">
                <img class="w-28 rounded-full mr-4" src="../assets/Photo-profil.jpeg" alt="Ma photo de profil">
                <div class="flex flex-col">
                    <span class="font-semibold text-xl tracking-tight">
                        Samuel Duflos
                    </span>
                    <span class="text-xs">
                        Développeur web
                    </span>
                </div>
            </div>
            <div class="block mt-5 sm:mt-0">
                <button @click.stop="toggle" class="relative flex items-center px-6 py-4 sm:px-6 sm:py-4 rounded-full border border-white cursor-pointer">
                    <svg class="w-6 h-6 text-white transition-transform duration-500" :class="[open ? 'transform : rotate-180' : 'transform : rotate-0']" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                        <path fill="currentColor" d="M233.4 105.4c12.5-12.5 32.8-12.5 45.3 0l192 192c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L256 173.3 86.6 342.6c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3l192-192z"/>
                    </svg>
                </button>
            </div>
        </div>
        <!-- <div class="block sm:hidden">
            <button @click="toggle" class="relative flex items-center px-3 py-2 rounded text-teal-lighter border-teal-light hover:text-white hover:border-white">
                <svg class="w-6 h-6 text-white transition-transform duration-1000" :style="{ transform: open ? 'rotate(180deg)' : 'rotate(0deg)' }" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <path fill="currentColor" d="M233.4 105.4c12.5-12.5 32.8-12.5 45.3 0l192 192c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L256 173.3 86.6 342.6c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3l192-192z"/>
                </svg>
            </button>
        </div> -->
        
        <div id="content-menu" @click.stop :class="[open ? 'max-h-screen opacity-100': 'max-h-0 opacity-0 hidden pointer-events-none']" class="flex flex-col animation-menu text-sm items-center md:items-start w-full">
            <div class="inline-block">
                <a href="#profile" @click.prevent="scrollToSection('profile')" class="no-underline mt-4 text-teal-lighter hover: text-white flex flex-col gap-1 md:flex-row flex-wrap items-center justify-center icon-shake">
                    <div class="w-10 h-10 mx-8 flex items-center justify-center border border-white-800 rounded-full">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
                            <path fill="white" d="M256 0l64 0c17.7 0 32 14.3 32 32l0 64c0 17.7-14.3 32-32 32l-64 0c-17.7 0-32-14.3-32-32l0-64c0-17.7 14.3-32 32-32zM64 64l128 0 0 48c0 26.5 21.5 48 48 48l96 0c26.5 0 48-21.5 48-48l0-48 128 0c35.3 0 64 28.7 64 64l0 320c0 35.3-28.7 64-64 64L64 512c-35.3 0-64-28.7-64-64L0 128C0 92.7 28.7 64 64 64zM176 437.3c0 5.9 4.8 10.7 10.7 10.7l202.7 0c5.9 0 10.7-4.8 10.7-10.7c0-29.5-23.9-53.3-53.3-53.3l-117.3 0c-29.5 0-53.3 23.9-53.3 53.3zM288 352a64 64 0 1 0 0-128 64 64 0 1 0 0 128z"/>
                        </svg>
                    </div>
                    <span class="font-bold text-md text-center">
                        Profil
                    </span>
                </a>
            </div>

            <div class="inline-block">
                <a href="#workExperiences" @click.prevent="scrollToSection('workExperiences')" class="no-underline mt-4 text-teal-lighter hover: text-white flex flex-col gap-1 md:flex-row flex-wrap items-center justify-center icon-shake">
                    <div class="w-10 h-10 mx-8 flex items-center justify-center border border-white-800 rounded-full">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path fill="white" d="M184 48l144 0c4.4 0 8 3.6 8 8l0 40L176 96l0-40c0-4.4 3.6-8 8-8zm-56 8l0 40L64 96C28.7 96 0 124.7 0 160l0 96 192 0 128 0 192 0 0-96c0-35.3-28.7-64-64-64l-64 0 0-40c0-30.9-25.1-56-56-56L184 0c-30.9 0-56 25.1-56 56zM512 288l-192 0 0 32c0 17.7-14.3 32-32 32l-64 0c-17.7 0-32-14.3-32-32l0-32L0 288 0 416c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-128z"/>
                        </svg>
                    </div>
                    <span class="font-bold text-md text-center">
                        Expériences professionnelles
                    </span>
                </a>
            </div>
                
            <div class="inline-block">
                <a href="#education" @click.prevent="scrollToSection('education')" class="no-underline block mt-4 text-teal-lighter hover: text-white flex flex-col gap-1 md:flex-row flex-wrap items-center justify-center icon-shake">
                    <div class="w-10 h-10 mx-8 flex items-center justify-center border border-white-800 rounded-full">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">
                            <path fill="white" d="M320 32c-8.1 0-16.1 1.4-23.7 4.1L15.8 137.4C6.3 140.9 0 149.9 0 160s6.3 19.1 15.8 22.6l57.9 20.9C57.3 229.3 48 259.8 48 291.9l0 28.1c0 28.4-10.8 57.7-22.3 80.8c-6.5 13-13.9 25.8-22.5 37.6C0 442.7-.9 448.3 .9 453.4s6 8.9 11.2 10.2l64 16c4.2 1.1 8.7 .3 12.4-2s6.3-6.1 7.1-10.4c8.6-42.8 4.3-81.2-2.1-108.7C90.3 344.3 86 329.8 80 316.5l0-24.6c0-30.2 10.2-58.7 27.9-81.5c12.9-15.5 29.6-28 49.2-35.7l157-61.7c8.2-3.2 17.5 .8 20.7 9s-.8 17.5-9 20.7l-157 61.7c-12.4 4.9-23.3 12.4-32.2 21.6l159.6 57.6c7.6 2.7 15.6 4.1 23.7 4.1s16.1-1.4 23.7-4.1L624.2 182.6c9.5-3.4 15.8-12.5 15.8-22.6s-6.3-19.1-15.8-22.6L343.7 36.1C336.1 33.4 328.1 32 320 32zM128 408c0 35.3 86 72 192 72s192-36.7 192-72L496.7 262.6 354.5 314c-11.1 4-22.8 6-34.5 6s-23.5-2-34.5-6L143.3 262.6 128 408z"/>
                        </svg>
                    </div>
                    <span class="font-bold text-md text-center">
                        Formation
                    </span>
                </a>
            </div>
                
            <div class="inline-block">
                <a href="#skills" @click.prevent="scrollToSection('skills')" class="no-underline block mt-4 text-teal-lighter hover: text-white flex flex-col gap-1 md:flex-row flex-wrap items-center justify-center icon-shake">
                    <div class="w-10 h-10 mx-8 flex items-center justify-center border border-white-800 rounded-full">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path fill="white" d="M495.9 166.6c3.2 8.7 .5 18.4-6.4 24.6l-43.3 39.4c1.1 8.3 1.7 16.8 1.7 25.4s-.6 17.1-1.7 25.4l43.3 39.4c6.9 6.2 9.6 15.9 6.4 24.6c-4.4 11.9-9.7 23.3-15.8 34.3l-4.7 8.1c-6.6 11-14 21.4-22.1 31.2c-5.9 7.2-15.7 9.6-24.5 6.8l-55.7-17.7c-13.4 10.3-28.2 18.9-44 25.4l-12.5 57.1c-2 9.1-9 16.3-18.2 17.8c-13.8 2.3-28 3.5-42.5 3.5s-28.7-1.2-42.5-3.5c-9.2-1.5-16.2-8.7-18.2-17.8l-12.5-57.1c-15.8-6.5-30.6-15.1-44-25.4L83.1 425.9c-8.8 2.8-18.6 .3-24.5-6.8c-8.1-9.8-15.5-20.2-22.1-31.2l-4.7-8.1c-6.1-11-11.4-22.4-15.8-34.3c-3.2-8.7-.5-18.4 6.4-24.6l43.3-39.4C64.6 273.1 64 264.6 64 256s.6-17.1 1.7-25.4L22.4 191.2c-6.9-6.2-9.6-15.9-6.4-24.6c4.4-11.9 9.7-23.3 15.8-34.3l4.7-8.1c6.6-11 14-21.4 22.1-31.2c5.9-7.2 15.7-9.6 24.5-6.8l55.7 17.7c13.4-10.3 28.2-18.9 44-25.4l12.5-57.1c2-9.1 9-16.3 18.2-17.8C227.3 1.2 241.5 0 256 0s28.7 1.2 42.5 3.5c9.2 1.5 16.2 8.7 18.2 17.8l12.5 57.1c15.8 6.5 30.6 15.1 44 25.4l55.7-17.7c8.8-2.8 18.6-.3 24.5 6.8c8.1 9.8 15.5 20.2 22.1 31.2l4.7 8.1c6.1 11 11.4 22.4 15.8 34.3zM256 336a80 80 0 1 0 0-160 80 80 0 1 0 0 160z"/>
                        </svg>
                    </div>
                    <span class="font-bold  text-md text-center">
                        Compétences
                    </span>
                </a>
            </div>
                
            <div class="inline-block">
                <a href="#interests" @click.prevent="scrollToSection('interests')" class="no-underline block mt-4 text-teal-lighter hover: text-white flex flex-col gap-1 md:flex-row flex-wrap items-center justify-center icon-shake">
                    <div class="w-10 h-10 mx-8 flex items-center justify-center border border-white-800 rounded-full">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">
                            <path fill="white" d="M274.9 34.3c-28.1-28.1-73.7-28.1-101.8 0L34.3 173.1c-28.1 28.1-28.1 73.7 0 101.8L173.1 413.7c28.1 28.1 73.7 28.1 101.8 0L413.7 274.9c28.1-28.1 28.1-73.7 0-101.8L274.9 34.3zM200 224a24 24 0 1 1 48 0 24 24 0 1 1 -48 0zM96 200a24 24 0 1 1 0 48 24 24 0 1 1 0-48zM224 376a24 24 0 1 1 0-48 24 24 0 1 1 0 48zM352 200a24 24 0 1 1 0 48 24 24 0 1 1 0-48zM224 120a24 24 0 1 1 0-48 24 24 0 1 1 0 48zm96 328c0 35.3 28.7 64 64 64l192 0c35.3 0 64-28.7 64-64l0-192c0-35.3-28.7-64-64-64l-114.3 0c11.6 36 3.1 77-25.4 105.5L320 413.8l0 34.2zM480 328a24 24 0 1 1 0 48 24 24 0 1 1 0-48z"/>
                        </svg>
                    </div>
                    <span class="font-bold text-md text-center">
                        Intérêts
                    </span>
                </a>
            </div>
                
            <div class="inline-block">
                <a href="#contact" @click.prevent="scrollToSection('contact')" class="no-underline block mt-4 text-teal-lighter hover: text-white flex flex-col gap-1 md:flex-row flex-wrap items-center justify-center icon-shake">
                    <div class="w-10 h-10 mx-8 flex items-center justify-center border border-white-800 rounded-full">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path fill="white" d="M96 0C60.7 0 32 28.7 32 64l0 384c0 35.3 28.7 64 64 64l288 0c35.3 0 64-28.7 64-64l0-384c0-35.3-28.7-64-64-64L96 0zM208 288l64 0c44.2 0 80 35.8 80 80c0 8.8-7.2 16-16 16l-192 0c-8.8 0-16-7.2-16-16c0-44.2 35.8-80 80-80zm-32-96a64 64 0 1 1 128 0 64 64 0 1 1 -128 0zM512 80c0-8.8-7.2-16-16-16s-16 7.2-16 16l0 64c0 8.8 7.2 16 16 16s16-7.2 16-16l0-64zM496 192c-8.8 0-16 7.2-16 16l0 64c0 8.8 7.2 16 16 16s16-7.2 16-16l0-64c0-8.8-7.2-16-16-16zm16 144c0-8.8-7.2-16-16-16s-16 7.2-16 16l0 64c0 8.8 7.2 16 16 16s16-7.2 16-16l0-64z"/>
                        </svg>
                    </div>
                    <span class="font-bold text-md text-center">
                        Contact
                    </span>
                </a>
            </div>
                
        </div>
    </nav>

</template>

<style scoped>
@keyframes shake {
    0%, 50%, 100% {
        transform: translateY(0);
    }
    25%, 75% {
        transform: translateY(-10px);
    }
}

.icon-shake:hover div {
    animation: shake 0.8s ease-in-out infinite;
}

.animation-menu {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    transition: all 1s ease-in-out;
}

</style>

<script setup>

    import { ref } from 'vue';

    const open = ref(false)

    const toggle = () => {
        open.value = !open.value
    }


    document.addEventListener('click', (e) => {
        console.log(e.target)
        if (!e.target.closest('header') && !e.target.closest('#content-menu')) {
            open.value = false;
        }
    })

    const scrollToSection = (sectionId) => {
        const section = document.getElementById(sectionId)
        if (section) {
            open.value = false;
            setTimeout(() => {
                const headerOffset = 50;
                const elementPosition = section.getBoundingClientRect().top;
                const offsetPosition = elementPosition + window.scrollY - headerOffset;

                window.scrollTo({
                    top: offsetPosition,
                    behavior: 'smooth'
                })
            }, 1000)
        }
    }

</script>