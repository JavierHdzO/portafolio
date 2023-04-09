<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar
        class="bg-cyan-8"
      >
        <q-btn
          flat
          dense
          round
          icon="las la-bars"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Francisco
        </q-toolbar-title>

        <div>v.1</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      :dark="true"
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

const essentialLinks = [
  {
    title: 'About',
    caption: 'A little about me',
    icon: 'las la-info',
    link: '#'
  },
  {
    title: 'Github',
    caption: 'github.com/JavierHdzO',
    icon: 'lab la-github',
    link: 'https://github.com/javierhdzo'
  },
  {
    title: 'Linkedin',
    caption: 'Francisco Javier Hdz O',
    icon: 'lab la-linkedin-in',
    link: 'https://www.linkedin.com/in/francisco-hernandez-ortiz/'
  },
  {
    title: 'Facebook',
    caption: '@SmJavier17',
    icon: 'lab la-facebook',
    link: 'https://www.facebook.com/SmJavier17'
  },
  {
    title: 'Email',
    caption: 'Send Personal Email',
    icon: 'las la-envelope',
    link: 'mailto:francisco.j.hdz.o@outlook.es?subject="Professional"&body="I am contact you to discuss professional business matter"'
  }
];

const leftDrawerOpen = ref(false)

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
