<template>
  <div class="defaultWrap">
    <AppHeader />
    <Nuxt class="page"/>
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from '../components/appHeader'
import AppFooter from '../components/appFooter'
export default {
  components:{
    AppHeader,
    AppFooter
  },
  data() {
    return {

    };
  },
  methods: {
  }
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

html,body,#__nuxt, #__layout, .defaultWrap{
  width: 100%;
  height: 100%;
}

.page{
  padding-top: 61px;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
