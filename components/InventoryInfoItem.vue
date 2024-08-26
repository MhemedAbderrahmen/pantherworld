<script setup lang="ts">
const props = defineProps<{
  icon: string;
  iconSecondary?: string;
  iconSecondaryAlt?: string;
  iconAlt: string;
  topText: string | number;
  bottomText: string;
}>();
</script>

<template>
  <div class="flex flex-row gap-4 bg-crust rounded-lg p-4 items-center">
    <div class="p-2 rounded-full bg-base text-base">
      <img :src="icon" height="32" width="32" :alt="iconAlt" />
    </div>
    <div class="flex flex-col gap-1">
      <p class="text-base capitalize font-bold">{{ topText }}</p>
      <div class="flex flex-row gap-1">
        <img :src="iconSecondary" v-if="iconSecondary" height="24" width="24" :alt="iconSecondaryAlt" />
        <p class="text-base">{{ bottomText }}</p>
      </div>
    </div>
  </div>
</template>
