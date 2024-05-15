<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Photo Gallery</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>

     <ion-content :fullscreen="true">
  <ion-fab vertical="bottom" horizontal="center" slot="fixed">
    <ion-fab-button @click="takePhoto()">
      <ion-icon :icon="camera"></ion-icon>
    </ion-fab-button>
  </ion-fab>
</ion-content>
    </ion-content>
  </ion-page>

<ion-content>
  <ion-grid>
    <ion-row>
      <ion-col size="6" :key="photo.filepath" v-for="photo in photos">
        <ion-img :src="photo.webviewPath"></ion-img>
      </ion-col>
    </ion-row>
  </ion-grid>

  <!-- <ion-fab> markup  -->
</ion-content>

</template>

<script setup lang="ts">
import {
  IonContent,
  IonCol,
  IonFab,
  IonFabButton,
  IonGrid,
  IonPage,
  IonHeader,
  IonIcon,
  IonImg,
  IonRow,
  IonTitle,
  IonToolbar,
} from '@ionic/vue';
import { camera, trash, close } from 'ionicons/icons';
import { usePhotoGallery } from '@/composables/usePhotoGallery';
import { usePhotoGallery, UserPhoto } from '@/composables/usePhotoGallery';
const { takePhoto } = usePhotoGallery();
const { photos, takePhoto } = usePhotoGallery();
</script>
