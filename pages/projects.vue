<template>
  <main class="min-h-screen">
    <AppHeader class="mb-12" title="Projets" :description="description" />
    <div class="space-y-4">
      <AppProjectCard
        v-for="(project, id) in projects"
        :key="id"
        :project="project"
      />
    </div>
  </main>
</template>

<script setup>
const description =
  "Découvrez les projets sur lesquels je travaille actuellement ou sur lesquels j’ai eu l’occasion de collaborer. Chacun reflète mon expertise et ma passion pour le développement web et la création d’applications sur mesure.";
useSeoMeta({
  title: "Projets | Mohamed Chettah",
  description,
});

const { data: projects } = await useAsyncData("projects-all", () =>
  queryContent("/projects").find()
);
</script>
