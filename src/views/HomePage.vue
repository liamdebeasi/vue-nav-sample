<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
        <ion-buttons slot="end">
          <ion-button id="open-modal">
            <ion-icon :icon="cog"></ion-icon>
          </ion-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <ion-modal
        :can-dismiss="true"
        :presenting-element="$parent.$refs.ionRouterOutlet"
        trigger="open-modal"
      >
        <Nav></Nav>
      </ion-modal>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { 
  IonContent, 
  IonHeader, 
  IonPage, 
  IonTitle, 
  IonToolbar,
  IonButtons,
  IonButton,
  IonIcon,
  IonModal,
} from '@ionic/vue';
import { cog } from 'ionicons/icons';
import { defineComponent } from 'vue';
import Nav from '@/components/Nav.vue';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButtons,
    IonButton,
    IonIcon,
    IonModal,
    Nav
  },
  setup() {
    return { cog }
  }
});
</script>
