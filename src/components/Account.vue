<template>
  <ion-header>
    <ion-toolbar>
      <ion-title>Account</ion-title>
      <ion-buttons slot="end">
        <ion-button @click="dismiss()">Done</ion-button>
      </ion-buttons>
    </ion-toolbar>
  </ion-header>
  <ion-content :fullscreen="true">
    <ion-list :inset="true">
      <ion-nav-link :component="Name">
        <ion-item :button="true">
          <ion-label>Name</ion-label>
        </ion-item>
      </ion-nav-link>
      <ion-nav-link :component="Email">
        <ion-item :button="true">
          <ion-label>Email</ion-label>
        </ion-item>
      </ion-nav-link>
      <ion-nav-link :component="Password">
        <ion-item :button="true">
          <ion-label>Password</ion-label>
        </ion-item>
      </ion-nav-link>
    </ion-list>
    
    <ion-list :inset="true">
      <ion-item :button="true" :detail="false">
        <ion-label>Sign Out</ion-label>
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
  IonButton,
  IonNavLink,
  modalController
} from '@ionic/vue';
import { defineComponent } from 'vue';
import Name from '@/components/Name.vue';
import Email from '@/components/Email.vue';
import Password from '@/components/Password.vue';

export default defineComponent({
  name: 'AccountComponent',
  components: {
    IonContent,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonList,
    IonItem,
    IonLabel,
    IonButtons,
    IonButton,
    IonNavLink
  },
  setup() {
    const dismiss = () => {
      modalController.dismiss();
    }
    return { dismiss, Name, Email, Password }
  }
});
</script>
