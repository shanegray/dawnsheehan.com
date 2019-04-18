<template>
  <section>
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
          thumbnailUrl: 'https://via.placeholder.com/600.png/FF0000',
          slug: 'painting-one'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: 'https://via.placeholder.com/800.png/00FF00',
          slug: 'painting-two'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: 'https://via.placeholder.com/250.png/0000FF',
          slug: 'painting-three'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: 'https://via.placeholder.com/450.png/FF0000',
          slug: 'painting-four'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: 'https://via.placeholder.com/300.png/FF0000',
          slug: 'painting-five'
        },
        {
          title: 'Painting Two',
          price: '€12.00',
          thumbnailUrl: 'https://via.placeholder.com/700.png/FF0000',
          slug: 'painting-six'
        }
      ]
    }
  }
}
</script>
