<template>
  <q-layout view="lHh Lpr lFf">
    <q-toolbar class="text-accent">
      <div class="row align-center" style="width: 1200px; margin: 0 auto;" >
      <q-toolbar-title>Joaquim Jambo</q-toolbar-title>
        <q-tabs v-model="tab" shrink >
          <q-list v-for="(item, index) in itens" :key="index">
            <q-item>
            <q-tab :name="text+item.id" :label="item.title" :anchor="item.link" />
            </q-item>
            <span>{{ item.link }}</span>
          </q-list>
        </q-tabs>
        <q-btn flat round icon="menu" />
        </div>
    </q-toolbar>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { reactive, ref } from 'vue'
const tab = ref('')
const text = ref('')
text.value = 'tab'
const itens = reactive([
  {
    id: 1,
    title: 'Home',
    link: 'section1'
  },
  {
    id: 2,
    title: 'About',
    link: 'section2'
  },
  {
    id: 3,
    title: 'Skills',
    link: 'section3'
  },
  {
    id: 4,
    title: 'Service',
    link: 'section4'
  },
  {
    id: 5,
    title: 'Portfolio',
    link: 'section5'
  },
  {
    id: 6,
    title: 'Contact Me',
    link: 'section5'
  }
])
</script>
