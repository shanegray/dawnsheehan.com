<template>
  <div id="wrapper">
    <div id="side-bar">
      <logo />
      <social-links />
    </div>
    <main id="main">
      <nuxt />
    </main>
  </div>
</template>

<script>
import Logo from '@/components/Logo'
import SocialLinks from '@/components/SocialLinks'

export default {
  components: {
    Logo,
    SocialLinks
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
@media (max-width: 900px) {
  #wrapper {
    width: 95%;
    margin: 0;
    display: flex;
    flex-direction: column;
  }
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

@media (max-width: 900px) {
  #side-bar {
    top: auto;
    bottom: auto;
    position: relative;
    padding-top: 1rem;
    width: 100%;
  }
}

#main {
  margin-left: 13.75rem;
  padding: 3.125rem 0;
}
@media (max-width: 900px) {
  #main {
    width: 95%;
    margin: 0 auto;
    padding: 0;
  }
}
</style>
