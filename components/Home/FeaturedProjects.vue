<template>
  <div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-6">
      PROJETS MIS EN AVANT
    </h2>
    <div class="space-y-4">
      <AppProjectCard
        v-for="(project, id) in projects"
        :key="id"
        :project="project"
      />
    </div>
    <div class="flex items-center justify-center mt-6 text-sm">
      <UButton
        label="Tous mes projets &rarr;"
        to="/projects"
        variant="link"
        color="gray"
      />
    </div>
  </div>
</template>

<script lang="ts" setup>
const { data: projects } = useAsyncData("projects-home", () =>
  queryContent("/projects").limit(2).find()
);
</script>
