<template>
  <ion-header>
    <ion-toolbar>
      <ion-buttons slot="start">
        <ion-back-button></ion-back-button>
      </ion-buttons>
      <ion-title>Email</ion-title>
      <ion-buttons slot="end">
        <ion-button @click="dismiss()">Done</ion-button>
      </ion-buttons>
    </ion-toolbar>
  </ion-header>
  <ion-content :fullscreen="true">
    <ion-list :inset="true">
      <ion-item>
        <ion-label>Email</ion-label>
        <ion-input></ion-input>
      </ion-item>
    </ion-list>
  </ion-content>
</template>

<script lang="ts">
import { 
  IonContent,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonList,
  IonItem,
  IonLabel,
  IonButtons,
  IonBackButton,
  IonInput,
  IonButton,
  modalController
} from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'EmailComponent',
  components: {
    IonContent,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonList,
    IonItem,
    IonLabel,
    IonButtons,
    IonBackButton,
    IonInput,
    IonButton,
  },
  setup() {
    const dismiss = () => {
      modalController.dismiss();
    }
    return { dismiss }
  }
});
</script>
