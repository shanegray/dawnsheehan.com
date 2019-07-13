<template>
  <div>
    <div class="image-list">
      <img
        v-for="image in filteredData"
        :key="image.name"
        :src="image.src"
        :alt="image.url"
        :srcset="image.sourceSet"
      />
    </div>
  </div>
</template>

<style scoped>
.image-header {
  background: lightgray;
  margin-bottom: 2rem;
  padding: 2rem;
}
.image-list {
  display: flex;
  flex-direction: column;
}
.image-list img {
  width: 95%;
  margin: 1rem auto;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.27), 0 0 40px rgba(0, 0, 0, 0.06) inset;
}
</style>

<script>
export default {
  data() {
    return {
      images: [
        {
          name: 'damhsa-1.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/damhsa-1.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_618/v1563014234/dawnsheehan/damhsa-1.jpg 618w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_435/v1563014234/dawnsheehan/damhsa-1.jpg 435w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014234/dawnsheehan/damhsa-1.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/damhsa-1.jpg'
        },
        {
          name: 'damhsa-2.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014228/dawnsheehan/damhsa-2.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_656/v1563014228/dawnsheehan/damhsa-2.jpg 656w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_450/v1563014228/dawnsheehan/damhsa-2.jpg 450w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014228/dawnsheehan/damhsa-2.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014228/dawnsheehan/damhsa-2.jpg'
        },
        {
          name: 'damhsa-3.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014227/dawnsheehan/damhsa-3.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_659/v1563014227/dawnsheehan/damhsa-3.jpg 659w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_537/v1563014227/dawnsheehan/damhsa-3.jpg 537w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_387/v1563014227/dawnsheehan/damhsa-3.jpg 387w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014227/dawnsheehan/damhsa-3.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014227/dawnsheehan/damhsa-3.jpg'
        },
        {
          name: 'damhsa.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563012658/dawnsheehan/damhsa.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_699/v1563012658/dawnsheehan/damhsa.jpg 699w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_633/v1563012658/dawnsheehan/damhsa.jpg 633w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_560/v1563012658/dawnsheehan/damhsa.jpg 560w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_487/v1563012658/dawnsheehan/damhsa.jpg 487w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_407/v1563012658/dawnsheehan/damhsa.jpg 407w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_316/v1563012658/dawnsheehan/damhsa.jpg 316w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563012658/dawnsheehan/damhsa.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563012658/dawnsheehan/damhsa.jpg'
        },
        {
          name: 'lakeshore-1.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014235/dawnsheehan/lakeshore-1.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_677/v1563014235/dawnsheehan/lakeshore-1.jpg 677w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_585/v1563014235/dawnsheehan/lakeshore-1.jpg 585w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_479/v1563014235/dawnsheehan/lakeshore-1.jpg 479w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_346/v1563014235/dawnsheehan/lakeshore-1.jpg 346w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014235/dawnsheehan/lakeshore-1.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014235/dawnsheehan/lakeshore-1.jpg'
        },
        {
          name: 'lakeshore.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014233/dawnsheehan/lakeshore.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_673/v1563014233/dawnsheehan/lakeshore.jpg 673w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_550/v1563014233/dawnsheehan/lakeshore.jpg 550w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_391/v1563014233/dawnsheehan/lakeshore.jpg 391w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014233/dawnsheehan/lakeshore.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014233/dawnsheehan/lakeshore.jpg'
        },
        {
          name: 'scribble-1.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014226/dawnsheehan/scribble-1.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_651/v1563014226/dawnsheehan/scribble-1.jpg 651w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_446/v1563014226/dawnsheehan/scribble-1.jpg 446w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014226/dawnsheehan/scribble-1.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014226/dawnsheehan/scribble-1.jpg'
        },
        {
          name: 'scribble.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014232/dawnsheehan/scribble.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_692/v1563014232/dawnsheehan/scribble.jpg 692w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_646/v1563014232/dawnsheehan/scribble.jpg 646w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_569/v1563014232/dawnsheehan/scribble.jpg 569w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_481/v1563014232/dawnsheehan/scribble.jpg 481w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_402/v1563014232/dawnsheehan/scribble.jpg 402w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_314/v1563014232/dawnsheehan/scribble.jpg 314w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014232/dawnsheehan/scribble.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014232/dawnsheehan/scribble.jpg'
        },
        {
          name: 'uaigneas-1.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014238/dawnsheehan/uaigneas-1.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_665/v1563014238/dawnsheehan/uaigneas-1.jpg 665w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_577/v1563014238/dawnsheehan/uaigneas-1.jpg 577w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_471/v1563014238/dawnsheehan/uaigneas-1.jpg 471w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_348/v1563014238/dawnsheehan/uaigneas-1.jpg 348w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014238/dawnsheehan/uaigneas-1.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014238/dawnsheehan/uaigneas-1.jpg'
        },
        {
          name: 'uaigneas-2.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014236/dawnsheehan/uaigneas-2.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_650/v1563014236/dawnsheehan/uaigneas-2.jpg 650w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_531/v1563014236/dawnsheehan/uaigneas-2.jpg 531w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_389/v1563014236/dawnsheehan/uaigneas-2.jpg 389w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014236/dawnsheehan/uaigneas-2.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014236/dawnsheehan/uaigneas-2.jpg'
        },
        {
          name: 'uaigneas.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/uaigneas.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_681/v1563014234/dawnsheehan/uaigneas.jpg 681w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_638/v1563014234/dawnsheehan/uaigneas.jpg 638w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_570/v1563014234/dawnsheehan/uaigneas.jpg 570w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_499/v1563014234/dawnsheehan/uaigneas.jpg 499w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_420/v1563014234/dawnsheehan/uaigneas.jpg 420w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_323/v1563014234/dawnsheehan/uaigneas.jpg 323w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014234/dawnsheehan/uaigneas.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/uaigneas.jpg'
        },
        {
          name: 'warriors-1.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014230/dawnsheehan/warriors-1.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_648/v1563014230/dawnsheehan/warriors-1.jpg 648w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_556/v1563014230/dawnsheehan/warriors-1.jpg 556w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_466/v1563014230/dawnsheehan/warriors-1.jpg 466w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_351/v1563014230/dawnsheehan/warriors-1.jpg 351w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014230/dawnsheehan/warriors-1.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014230/dawnsheehan/warriors-1.jpg'
        },
        {
          name: 'warriors-2.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/warriors-2.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_697/v1563014234/dawnsheehan/warriors-2.jpg 697w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_597/v1563014234/dawnsheehan/warriors-2.jpg 597w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_492/v1563014234/dawnsheehan/warriors-2.jpg 492w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_366/v1563014234/dawnsheehan/warriors-2.jpg 366w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014234/dawnsheehan/warriors-2.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014234/dawnsheehan/warriors-2.jpg'
        },
        {
          name: 'warriors-3.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014230/dawnsheehan/warriors-3.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_677/v1563014230/dawnsheehan/warriors-3.jpg 677w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_577/v1563014230/dawnsheehan/warriors-3.jpg 577w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_478/v1563014230/dawnsheehan/warriors-3.jpg 478w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_357/v1563014230/dawnsheehan/warriors-3.jpg 357w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014230/dawnsheehan/warriors-3.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014230/dawnsheehan/warriors-3.jpg'
        },
        {
          name: 'warriors.jpg',
          sourceSet:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014231/dawnsheehan/warriors.jpg 700w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_699/v1563014231/dawnsheehan/warriors.jpg 699w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_634/v1563014231/dawnsheehan/warriors.jpg 634w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_569/v1563014231/dawnsheehan/warriors.jpg 569w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_498/v1563014231/dawnsheehan/warriors.jpg 498w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_420/v1563014231/dawnsheehan/warriors.jpg 420w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_321/v1563014231/dawnsheehan/warriors.jpg 321w, https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_200/v1563014231/dawnsheehan/warriors.jpg 200w',
          src:
            'https://res.cloudinary.com/dzdl7auuv/image/upload/c_fill,g_auto/c_scale,w_700/v1563014231/dawnsheehan/warriors.jpg'
        }
      ]
    }
  },
  computed: {
    filteredData() {
      return this.images.filter(img =>
        img.name.startsWith(this.$route.params.slug)
      )
    },
    srcSet() {
      return this.images.map(img => img.sourceSet).join(', ')
    }
  }
}
</script>
