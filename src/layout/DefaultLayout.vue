<template>
 <Header @toggle-drawer="drawer = !drawer" />
 <NavigationDrawer v-model="drawer"/>

    <v-main>
    <router-view />
    </v-main>

</template>

<script setup lang="ts">
import { ref } from 'vue'
import Header from '@/components/layout/Header.vue'
import NavigationDrawer from '@/components/layout/NavigationDrawer.vue';

const drawer = ref(false)
</script>

 
