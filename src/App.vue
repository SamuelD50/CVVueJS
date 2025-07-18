<script setup>
  import Header from './components/Header.vue';
  import WorkExperiences from './components/WorkExperiences.vue';
  import Education from './components/Education.vue';
  import Skills from './components/Skills.vue';
  import Interests from './components/Interests.vue';
  import Contact from './components/Contact.vue';
  import AdditionalInformation from './components/AdditionalInformation.vue';
  import Footer from './components/Footer.vue';
</script>


<template>
  <Header />

  <main class="flex">
    <section class="w-2/5 flex flex-col items-center -mt-28 mx-5 bg-blue-500 rounded-t-full">
      <img class="w-56 aspect-square m-5 rounded-full object-cover" src="./assets/Photo-profil.jpeg" alt="Photo">
      <ul class="flex flex-col items-center gap-1 my-2 font-medium text-white font-semibold">
        <li>
          Sens du relationnel
        </li>
        <li>
          Organisé
        </li>
        <li>
          Persévérant
        </li>
      </ul>
      <Contact/>
      <Skills />
      <Interests />
      <AdditionalInformation />
    </section>

    <section class="w-3/5">
      <WorkExperiences />
      <Education />
    </section>
  </main>

<!--   <Footer /> -->
</template>