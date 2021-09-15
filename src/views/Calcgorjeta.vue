<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Calculadora de Gorjeta</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Calculadora de Gorjeta</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <ExploreContainer name="Calculadora de Gorjeta page" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';

export default  {
  name: 'Calculadora de Gorjeta',
  components: { ExploreContainer, IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
}
</script>