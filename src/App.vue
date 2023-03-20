<template>
  <SomeSlotComponent>
    <div>
      <div>
        <h1>Edit this text in template and then click save</h1>
        <h2>Hotreload will fail with error in console</h2>
      </div>

      <span v-if="loading">loading</span>
    </div>
  </SomeSlotComponent>
</template>

<script setup>
// SomeSlotComponent is very basic and just renders slot content inside a colored div:
import { SomeSlotComponent } from '@doeke/some-component-library';
import { onMounted, ref } from 'vue';

const loading = ref(true);

onMounted(() => {
  loading.value = false;
});
</script>
