<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 2</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>

      <ExploreContainer name="Tab 2 page" />
      <RouterLink
        :to="{
          name: 'Tab2Subpage',
          query: {
            test: 'this-is-a-test-value',
          },
        }"
        >Go to: /tabs/tab2/subpage</RouterLink
      >
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from "@ionic/vue"
import ExploreContainer from "@/components/ExploreContainer.vue"
import { RouterLink } from "vue-router"

export default {
  name: "Tab2",
  components: {
    ExploreContainer,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
    RouterLink,
  },
}
</script>
