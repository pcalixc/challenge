<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import { LottieAnimation } from 'lottie-web-vue'
import Loading from '@/assets/Loading.json'
import { useEmailsStore } from '@/stores/emails'
const emailsStore = useEmailsStore()
</script>

<template>
  <div
  v-if="!emailsStore.ServerErrorResponse.errorStatus"
   class="h-full flex justify-center align-middle mt-24">
    <lottie-animation :animation-data="Loading" :loop="true" class="w-60 h-60" />
  </div>
</template>
