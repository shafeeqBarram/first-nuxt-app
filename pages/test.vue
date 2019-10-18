<template>
    <div>
        {{ $t('ForgotCard') }}
        <nuxt-link :to="localePath('test', 'en')">test page in English</nuxt-link>
        <nuxt-link :to="localePath('test', 'de')">test page in German</nuxt-link>
        <div>
          <h1>Lang navigation</h1>
            <nuxt-link :to="switchLocalePath('de')">Deutsch</nuxt-link>
            <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
        </div>
    </div>
</template>
<script>
import commonMessage from './i18n.vue';
export default {
          i18n: {
      sharedMessages: commonMessage
    },
    methods:{
    }

}
</script>
