<template>
  <ion-page>
    <ion-content>
      <ion-tabs>
        <ion-router-outlet></ion-router-outlet>
        <ion-tab-bar slot="bottom">
          <ion-tab-button tab="groceries" href="/groceries">
            <ion-icon :icon="bag"/>
            <ion-label>Groceries</ion-label>
          </ion-tab-button>

          <ion-tab-button tab="about" href="/about">
            <ion-icon :icon="people"/>
            <ion-label>About</ion-label>
          </ion-tab-button>

          <ion-tab-button tab="contact" href="/contact">
            <ion-icon :icon="help"/>
            <ion-label>Contact</ion-label>
          </ion-tab-button>
        </ion-tab-bar>
      </ion-tabs>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonTabBar,
  IonTabButton,
  IonTabs,
  IonContent,
  IonLabel,
  IonIcon,
  IonPage,
  IonRouterOutlet,
} from '@ionic/vue';
import {bag, people, help} from 'ionicons/icons';

export default {
  name: 'HomePage',
  components: {
    IonContent,
    IonLabel,
    IonTabs,
    IonTabBar,
    IonTabButton,
    IonIcon,
    IonPage,
    IonRouterOutlet,
  },
  setup() {
    return {
      bag,
      people,
      help,
    };
  },
};
</script>