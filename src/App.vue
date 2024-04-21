<script setup>
import SlotComponent from './components/SlotComponent.vue'
import FallbackContent from './components/FallbackContent.vue'
import NamedSlot from './components/NamedSlot.vue'
import DefaultSlot from './components/DefaultSlot.vue'
</script>

<template>
  <h1>Slot</h1>
  <SlotComponent>
    <h1>Content 1</h1>
    <h1>Content 2</h1>
  </SlotComponent>

  <hr>
  <FallbackContent />
  <FallbackContent>
    <h1>Fallback will not work because I'm providing content inside component</h1>
  </FallbackContent>

  <hr>
  <NamedSlot>
    <!-- v-slot:header -->
    <template v-slot:header>
      <h1>Header</h1>
    </template>
    <!-- #content -->
    <template #content>
      <p>Content</p>
    </template>
  </NamedSlot>

  <hr>
  <!-- Default content with NamedSlot -->
  <NamedSlot>
    <template #header></template>
    <template #content></template>
  </NamedSlot>

  <hr>
  <DefaultSlot>
    <template #default>
      <h1>This is some random default content</h1>
    </template>
  </DefaultSlot>
</template>

<style scoped></style>