<script setup>
import { useCommonStore } from '../stores/common'

const commonStore = useCommonStore()

const versionText = PACKAGE_NAME + ' @ ' + APP_VERSION
</script>

<template>
  <main>
    <v-btn :to="{ name: 'settings_create' }" :disabled="commonStore.isDeviceOffline.value">
      Neues Rezept hinzufügen
    </v-btn>
    <div>
      {{ versionText }}
      <a href="https://github.com/" target="_blank">github</a>
    </div>
  </main>
</template>

<style scoped></style>
