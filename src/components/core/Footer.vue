<template>
  <v-footer
    id="core-footer"
    absolute
    height="82"
  >
    <v-spacer/>
    <span class="font-weight-light copyright">
      <strong v-if="environment !== 'PRODUCTION'">{{ environment }}</strong>
      {{ $t('App.name') }} {{ packageJson.version }} &copy; 2008-{{ (new Date()).getFullYear() }} {{ $t('App.footer') }}
    </span>
  </v-footer>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    ...mapState(['packageJson', 'environment'])
  }
}
</script>
