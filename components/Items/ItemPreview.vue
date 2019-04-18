<template>
  <nuxt-link :to="slug">
    <article>
      <img class="image" :src="thumbnailUrl" :alt="title" />
      <span>{{ title }}</span>
      <span>{{ price }}</span>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    price: {
      type: String,
      required: false,
      default: ''
    },
    thumbnailUrl: {
      type: String,
      required: false,
      default: ''
    },
    slug: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
a {
  display: block;
  text-decoration: none;
  color: black;
  margin-bottom: 2rem;
}

article {
  display: flex;
  flex-direction: column;
}
</style>
