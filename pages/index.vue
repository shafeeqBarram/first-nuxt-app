<template>
  <div>
<nuxt-link :to="localePath('test', 'en')">test page in English</nuxt-link>
<div>
  <h1>Lang navigation</h1>
    <nuxt-link :to="switchLocalePath('de')">Deutsch</nuxt-link>
    <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
</div>
{{ $t('Present') }}  {{$i18n.locale}}
  </div>
</template>

<script>
import commonMessage from './i18n.vue';
export default {
  components: {
  },
      i18n: {
      sharedMessages: commonMessage
    },
    computed: {
  availableLocales () {
    // return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale)
  }
  }
}
</script>

<style>
</style>
