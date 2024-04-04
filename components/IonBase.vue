<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button color="secondary" text="" />
        </ion-buttons>
        <ion-buttons slot="end">
          <ion-menu-button color="primary" />
        </ion-buttons>
        <ion-title>{{ title }}</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="contentFullscreen">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">{{ title }}</ion-title>
        </ion-toolbar>
      </ion-header>
      <div :class="noContentPadding ? '' : 'ion-padding'">
        <slot />
      </div>
    </ion-content>
  </ion-page>
</template>
<script setup lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonButtons,
  IonBackButton,
  IonMenuButton,
  IonTitle,
  IonContent,
} from '@ionic/vue'

interface Props {
  title: string
  noContentPadding?: boolean
  contentFullscreen?: boolean
}

withDefaults(defineProps<Props>(), {
  noContentPadding: false,
  contentFullscreen: true,
})
</script>
