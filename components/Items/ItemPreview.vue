<template>
  <nuxt-link :to="slug">
    <article>
      <img class="image" :src="thumbnailUrl" :alt="title" />
      <div class="image-text">
        <span>{{ title }}</span>
        <span>{{ price }}</span>
        <div>
          <em>Shane will fix this later</em>
        </div>
      </div>
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
  margin-bottom: 3rem;
}

article {
  display: flex;
  flex-direction: column;
  border-radius: 7px 7px 7px 7px;
  box-shadow: 0px 14px 32px 0px rgba(0, 0, 0, 0.5);
}

article img {
  width: 100%;
  border-radius: 7px 7px 0px 0px;
}
.image-text {
  display: flex;
  justify-content: space-around;
  padding: 2rem;
}
</style>
