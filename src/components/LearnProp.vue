<template>
  <BaseSection>
    <div class="justify-content-center align-items-center d-flex">
      <AppButton :processing="true">Submit</AppButton>
    </div>
  </BaseSection>
</template>

<script setup>
import BaseSection from './BaseSection.vue'
import AppButton from './AppButton.vue'

</script>
