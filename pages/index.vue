<template>
  <section>
    <blurb />
    <item-preview
      v-for="image in images"
      :key="image.slug"
      :title="image.title"
      :slug="image.slug"
      :price="image.price"
      :srcset="image.sourceSet"
    />
  </section>
</template>

<script>
import ItemPreview from '@/components/Items/ItemPreview'
import Blurb from '@/components/Blurb'

export default {
  components: {
    ItemPreview,
    Blurb
  },
  data() {
    return {
      images: [
        {
          name: 'damhsa.jpg',
          slug: 'damhsa',
          title: 'Damhsa',
          price: '€50.00',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563012658/dawnsheehan/damhsa.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_699/v1563012658/dawnsheehan/damhsa.jpg 699w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_633/v1563012658/dawnsheehan/damhsa.jpg 633w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_560/v1563012658/dawnsheehan/damhsa.jpg 560w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_487/v1563012658/dawnsheehan/damhsa.jpg 487w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_407/v1563012658/dawnsheehan/damhsa.jpg 407w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_316/v1563012658/dawnsheehan/damhsa.jpg 316w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563012658/dawnsheehan/damhsa.jpg 200w'
        },
        {
          name: 'lakeshore.jpg',
          slug: 'lakeshore',
          title: 'Lakeshore',
          price: '€50.00',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014233/dawnsheehan/lakeshore.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_673/v1563014233/dawnsheehan/lakeshore.jpg 673w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_550/v1563014233/dawnsheehan/lakeshore.jpg 550w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_391/v1563014233/dawnsheehan/lakeshore.jpg 391w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014233/dawnsheehan/lakeshore.jpg 200w'
        },
        {
          name: 'scribble.jpg',
          slug: 'scribble',
          title: 'Scribble',
          price: '€50.00',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014232/dawnsheehan/scribble.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_692/v1563014232/dawnsheehan/scribble.jpg 692w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_646/v1563014232/dawnsheehan/scribble.jpg 646w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_569/v1563014232/dawnsheehan/scribble.jpg 569w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_481/v1563014232/dawnsheehan/scribble.jpg 481w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_402/v1563014232/dawnsheehan/scribble.jpg 402w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_314/v1563014232/dawnsheehan/scribble.jpg 314w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014232/dawnsheehan/scribble.jpg 200w'
        },
        {
          name: 'uaigneas.jpg',
          slug: 'uaigneas',
          title: 'Uaigneas',
          price: '€50.00',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/uaigneas.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_681/v1563014234/dawnsheehan/uaigneas.jpg 681w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_638/v1563014234/dawnsheehan/uaigneas.jpg 638w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_570/v1563014234/dawnsheehan/uaigneas.jpg 570w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_499/v1563014234/dawnsheehan/uaigneas.jpg 499w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_420/v1563014234/dawnsheehan/uaigneas.jpg 420w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_323/v1563014234/dawnsheehan/uaigneas.jpg 323w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014234/dawnsheehan/uaigneas.jpg 200w'
        },
        {
          name: 'warriors.jpg',
          slug: 'warriors',
          title: 'Warriors',
          price: '€50.00',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014231/dawnsheehan/warriors.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_699/v1563014231/dawnsheehan/warriors.jpg 699w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_634/v1563014231/dawnsheehan/warriors.jpg 634w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_569/v1563014231/dawnsheehan/warriors.jpg 569w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_498/v1563014231/dawnsheehan/warriors.jpg 498w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_420/v1563014231/dawnsheehan/warriors.jpg 420w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_321/v1563014231/dawnsheehan/warriors.jpg 321w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014231/dawnsheehan/warriors.jpg 200w'
        }
      ]
    }
  }
}
</script>
