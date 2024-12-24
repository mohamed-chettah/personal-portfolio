<template>
  <div class="space-y-6">
    <NuxtImg src="/avatar.png" alt="Mohamed Chettah"
      class="ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
      sizes="48px sm:64px" placeholder format="webp" />
    <h1 class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100">
      Salut !
    </h1>
    <p class="text-gray-900 dark:text-gray-400">
      Je m'appelle Mohamed, Développeur web Full-Stack basé en France. <br>
      Je suis spécialisé dans la création d'applications web et de sites utilisant Nuxt et Laravel.
      J'ai créé ce portfolio pour partager mes projets, mes expériences, et mes réflexions (principalement sur la tech et le design).
    </p>
    <p class="text-gray-900 dark:text-gray-400">

      La journée, je jongle entre mes cours à <a href="https://www.esgi.fr/" target="_blank" class="underline">l'ESGI</a> et mon alternance chez <a href="https://www.monabee.fr/" target="_blank" class="underline">Monabee</a>, où je mets en pratique tout ce que j'apprends.
      Le soir (et les week-ends), j'aime expérimenter de nouveaux outils et transformer mes idées en code.
    </p>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "Mohamed Chettah",
  description:
    "I'm Fayaz, your friendly neighborhood software, product engineer and designer from Bengaluru, India. I specialize in building web applications and sites using Javascript, React, Vue & Node.",
});
</script>
