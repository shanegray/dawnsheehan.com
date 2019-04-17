<template>
  <div id="wrapper">
    <div id="side-bar">
      <logo />
      <page-links />
      <social-links />
    </div>
    <main id="main">
      <blurb />
      <nuxt />
    </main>
  </div>
</template>

<script>
import Logo from '@/components/Logo'
import PageLinks from '@/components/PageLinks'
import SocialLinks from '@/components/SocialLinks'
import Blurb from '@/components/Blurb'

export default {
  components: {
    Logo,
    PageLinks,
    SocialLinks,
    Blurb
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
#wrapper {
  width: 900px;
  margin: 2rem auto;
  display: flex;
}

#main {
  flex: 1 auto;
}
</style>
