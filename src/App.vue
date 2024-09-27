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

  <main class="bg-lightGreen py-4 flex flex-row justify-around flex-wrap">

    
    <div class="flex flex-col px-10 flex-wrap md:w-1/2 w-full">
      <WorkExperiences />
      <Education />
    </div>

    <div class="flex flex-col px-10 flex-wrap md:w-1/2 w-full">
      <Skills />
      <Profile />
      <Interests />
      <Contact/>
    </div>
  </main>
</template>

<!-- <template>
  <header class="bg-blue-500">
    <Header/>
  </header>

  <main class="flex flex-row bg-gray-300">
    <div>
      <Profile/>
      <WorkExperiences/>
    </div>
    <div>
      <Education/>
      <Skills/>
    </div>
    <div>
      <Interests/>
    </div>
    
  </main>

  <footer class="bg-green-300">
    <Contact/>

  </footer>
</template> -->


<!-- <style scoped>
header {
  background-color: blue;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

footer {
  background-color: green;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style> -->
