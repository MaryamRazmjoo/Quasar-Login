<template>
  <q-layout view="hHh lpR fFf">
    <q-header
      class="bg-purple text-white"
    >
      <q-toolbar>
      </q-toolbar>
      <q-tabs align="center">
        <q-route-tab to="/signIn" label="ثبت نام"/>
        <q-route-tab to="/logIn" label="ورود"/>
      </q-tabs>
    </q-header>
    <q-page-container>
      <router-view/>
    </q-page-container>

  </q-layout>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MainLayout',
  components: {}
})
</script>
