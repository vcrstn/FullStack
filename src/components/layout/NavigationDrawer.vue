<template>
  <v-navigation-drawer
    v-model="drawer"
    :location="$vuetify.display.mobile ? 'bottom' : undefined"
    temporary
  >
    <v-list
      v-model:selected="group"
      :items="items"
    />
  </v-navigation-drawer>
</template>

<script setup lang="ts">
  import { computed, ref, watch } from 'vue'

  const props = defineProps<{
    modelValue: boolean
  }>()

  const emit = defineEmits<{
    (event: 'update:modelValue', value: boolean): void
  }>()

  const drawer = computed({
    get: () => props.modelValue,
    set: (value: boolean) => emit('update:modelValue', value),
  })

  const group = ref<string[]>([])

  const items = [
    {
      title: 'Foo',
      value: 'foo',
    },
    {
      title: 'Bar',
      value: 'bar',
    },
    {
      title: 'Fizz',
      value: 'fizz',
    },
    {
      title: 'Buzz',
      value: 'buzz',
    },
  ]

  watch(group, () => {
    drawer.value = false
  })
</script>
