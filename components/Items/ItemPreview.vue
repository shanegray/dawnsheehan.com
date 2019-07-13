<template>
  <nuxt-link :to="slug">
    <article>
      <img class="image" :src="src" :alt="title" :srcset="srcset" />
      <div class="image-text">
        <span>{{ title }}</span>
        <span>{{ price }}</span>
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
    slug: {
      type: String,
      required: true
    },
    srcset: {
      type: String,
      required: true
    }
  },
  computed: {
    src() {
      return `https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/${
        this.slug
      }.jpg`
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
