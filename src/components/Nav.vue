<template>
  <ion-nav :root="Account"></ion-nav>
</template>

<script lang="ts">
import { 
  IonNav
} from '@ionic/vue';
import { defineComponent } from 'vue';
import Account from '@/components/Account.vue';

export default defineComponent({
  name: 'NavComponent',
  components: {
    IonNav
  },
  setup() {
    return { Account }
  }
});
</script>
