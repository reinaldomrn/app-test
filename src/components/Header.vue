<template>
  <q-header elevated class="glossy">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
          icon="menu"
        />

        <q-toolbar-title>
          Test App
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>

<style>

</style>
