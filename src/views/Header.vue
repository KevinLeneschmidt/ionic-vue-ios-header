<template>
  <ion-base title="Header">
    <p>Header Page</p>
    <ion-button router-link="/home">Go back to home</ion-button>
  </ion-base>
</template>
<script setup lang="ts">
import IonBase from '@/components/IonBase.vue'

import { IonButton } from '@ionic/vue'
</script>
