<script setup lang="ts">
  const callToActions = [
    {
      img: 'https://images.unsplash.com/photo-1585664811087-47f65abbad64',
      action: 'Adopt',
      to: '/adopt',
    },
    {
      img: 'https://images.unsplash.com/photo-1499946682598-202f5b527154',
      action: 'Volunteer',
      to: '/volunteer',
    },
    {
      img: 'https://images.unsplash.com/photo-1415369629372-26f2fe60c467',
      action: 'Donate',
      to: '/quick-start',
    },
  ]
</script>
<template>
  <section class="container mx-auto px-4 py-12">
    <div>
      <h6 class="text-primary-600 dark:text-primary-200 text-center uppercase">
        Get Involved
      </h6>
      <h3 class="capitalize mt-3 text-center">
        Small gesture for a big impact
      </h3>
      <p class="mt-4 text-center">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </p>
    </div>
    <div class="-mx-4 flex flex-wrap justify-center mt-12">
      <CallToActionCard
        v-for="(callToAction, index) in callToActions"
        :key="index"
        :action="callToAction.action"
        :img="callToAction.img"
        :to="callToAction.to"
      />
    </div>
  </section>
</template>
<style scoped></style>
