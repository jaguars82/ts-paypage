<template>
  <div>
    {{www}}
    <div
      v-for="provider of payProviders"
      :key="provider.id"
    >
      <p>{{ provider.name }}</p>
      <img :src="provider.logo">
    </div>
  </div>
</template>

<script>
import {ref, reactive} from 'vue'
import {providers} from '../data/data.js'

export default {
  name: "PayProviderCard",
  setup() {
    const www = ref('dsds')
    const payProviders = reactive(providers)

    return {
      payProviders,
      www
    }
  }
}

</script>