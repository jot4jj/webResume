<script setup lang="ts">
  import HeroSection from './components/HeroSection.vue';
  import ExperienceTimeline from './components/ExperienceTimeline.vue';
  import Stack from './components/Stack.vue';
  import ProjectCard from './components/ProjectCard.vue';
  import Menu from './components/Menu.vue';
</script>

<template>
  <div class="min-h-screen flex flex-col items-center z-50">
    <div class="my-4">
      <Menu />
    </div>

    <main class="container justify-center place-items-center mx-auto space-y-16 w-3/4">
      <HeroSection/>
      <ExperienceTimeline/>
      <Stack />
      <ProjectCard />
    </main>
  </div>
</template>
