<template>
  <main class="min-h-screen">
    <AppHeader
      class="mb-12"
      title="Ce que j'utilise au quotidien"
      :description="description"
    />
    <div class="space-y-24">
      <ul class="space-y-8">
        <AppUsesHeader title="Equipement" />
        <AppUsesItem v-for="(item, id) in hardware" :key="id" :item="item" />
      </ul>
      <ul class="space-y-8">
        <AppUsesHeader title="Logiciels" />
        <AppUsesItem v-for="(item, id) in software" :key="id" :item="item" />
      </ul>
      <ul class="space-y-8">
        <AppUsesHeader title="Ordinateur" />
        <AppUsesItem v-for="(item, id) in desk" :key="id" :item="item" />
      </ul>
      <ul class="space-y-8">
        <AppUsesHeader title="Autres" />
        <AppUsesItem v-for="(item, id) in other" :key="id" :item="item" />
      </ul>
    </div>
  </main>
</template>

<script setup>
const description =
  "Les logiciels que j'utilise, les gadgets que j'apprécie et d'autres outils que je recommande. Voici une grande liste de toutes mes ressources préférées ! "
useSeoMeta({
  title: "Ce que j'utilise | Mohamed Chettah",
  description,
});
const { data: items } = await useAsyncData("uses", () =>
  queryContent("/uses").find()
);
const hardware = items.value.filter((item) => item.category === "hardware");
const software = items.value.filter((item) => item.category === "software");
const desk = items.value.filter((item) => item.category === "desk");
const other = items.value.filter((item) => item.category === "others");
</script>
