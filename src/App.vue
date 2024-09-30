<script setup>
  import Header from './components/Header.vue';
  import Profile from './components/Profile.vue';
  import WorkExperiences from './components/WorkExperiences.vue';
  import Education from './components/Education.vue';
  import Skills from './components/Skills.vue';
  import Interests from './components/Interests.vue';
  import Contact from './components/Contact.vue';
</script>


<template>
  
  <header class="bg-blue-500 px-2 py-4 text-white">
    <Header/>
  </header>

  <main class="bg-lightGreen py-4 px-5 flex flex-row justify-around flex-wrap">

    
    <div class="flex flex-col flex-wrap md:w-1/2 w-full">
      <Profile />
      <WorkExperiences />
      <Education />
    </div>

    <div class="flex flex-col flex-wrap md:w-1/2 w-full">
      <Skills />
      <Interests />
      <Contact/>
    </div>
  </main>
</template>
