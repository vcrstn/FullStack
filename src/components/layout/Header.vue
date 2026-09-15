<template>
  <v-app-bar
    color="primary"
    density="compact"
  >
    <template #prepend>
      <v-app-bar-nav-icon
        @click="toggleDrawer"
      />
    </template>

    <v-app-bar-title>Photos</v-app-bar-title>

    <template #append>
      <v-btn icon="mdi-dots-vertical" />
    </template>
  </v-app-bar>
</template>

<script setup lang="ts">
const emit = defineEmits<{
  (event: 'toggle-drawer'): void
}>()

function toggleDrawer() {
  console.log('HAMBURGER CLICKED')
  emit('toggle-drawer')
}
</script>