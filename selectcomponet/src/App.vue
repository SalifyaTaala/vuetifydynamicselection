<template>
  <v-app>
    <v-main>
      <SelectOptions/>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import SelectOptions from './components/selectOptions.vue'

@Component({
  components: { SelectOptions }
})
export default class App extends Vue {}
</script>
