<template>
  <section>
    <!-- <img src="~/assets/img/one.jpg" /> -->
    <item-preview
      v-for="item in items"
      :key="item.slug"
      :title="item.title"
      :slug="item.slug"
      :price="item.price"
      :thumbnail-url="item.thumbnailUrl"
    />
  </section>
</template>

<script>
import ItemPreview from '@/components/Items/ItemPreview'

export default {
  components: {
    ItemPreview
  },
  data() {
    return {
      items: [
        {
          title: 'Painting One',
          price: '€30.00',
          thumbnailUrl: require('~/assets/img/one.jpg'),
          slug: 'painting-one'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: require('~/assets/img/two.jpg'),
          slug: 'painting-two'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: require('~/assets/img/three.jpg'),
          slug: 'painting-three'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: require('~/assets/img/four.jpg'),
          slug: 'painting-four'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: require('~/assets/img/five.jpg'),
          slug: 'painting-five'
        }
      ]
    }
  }
}
</script>
