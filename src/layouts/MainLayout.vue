<template>
  <q-layout> 
    <Header />   
    <q-page-container >
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import Header from 'components/Header.vue'

export default {
  name: 'MainLayout',
  components: { Header },  
}
</script>
