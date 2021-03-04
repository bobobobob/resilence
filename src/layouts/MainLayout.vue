<template>
  <q-layout view="hHr lpR lfr">
    <q-header>
      <top-bar />
    </q-header>

    <q-page-container style="max-width: 960px; margin: auto;">
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import TopBar from 'src/components/TopBar.vue'
export default {
  components: { TopBar },
  name: 'MainLayout',

  data () {
    return {}
  }
}
</script>
