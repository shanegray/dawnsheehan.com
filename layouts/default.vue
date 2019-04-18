<template>
  <div id="wrapper">
    <div id="side-bar">
      <logo />
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
import SocialLinks from '@/components/SocialLinks'
import Blurb from '@/components/Blurb'

export default {
  components: {
    Logo,
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

body {
  background-color: #f7fcf4;
}

#wrapper {
  width: 900px;
  margin: 0 auto;
}

#side-bar {
  position: fixed;
  width: 13.75rem;
  bottom: 0;
  top: 0;

  display: flex;
  flex-direction: column;
  text-align: center;

  padding-top: 10rem;
}

#main {
  margin-left: 13.75rem;
  padding: 3.125rem 0;
}
</style>
