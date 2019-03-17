<template>
  <section class="gallery">
    <div v-for="(image, index) in images" class="figure item" :key="`image-${index}`">
      <figure>
        <img :src="image.url" />
        <div class="caption-wrapper">
          <figcaption>
            {{ image.caption }}
            <span class="photoby">Foto: Svein Stølen</span>
          </figcaption>
        </div>
      </figure>
    </div>
    <nav class="gallery-nav">
      <img v-for="(image, index) in images" :key="`image-${index}`" :src="image.url" />
    </nav>
  </section>
</template>

<script>
export default {
  name: 'ImageGallery',
  props: {
    images: Array
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';
.gallery {
  padding: 0;
}
div {
  margin: 0 auto;
  width: 100%;
  position: relative;

  figure {
    margin: 0;
    padding: 0;
  }

  img {
    height: 80vh;
    width: 100%;
    object-fit: cover;
    z-index: 1000;
  }

  .caption-wrapper {
    position: absolute;
    top: 1rem;
    left: 1rem; right: 1rem; bottom: 1rem;
    z-index: 1001;
  }

  figcaption {
    padding: 0.6rem 1rem;
    max-width: $width-s;
    margin: 0;
    position: absolute;
    bottom: 0;
    background: $color-black;
    color: $color-white;
  }
  .photoby {
    font-size: $font-xs;
    display: block;
    font-style: italic;
    text-align: right;
    font-family: $sans-serif;
  }
}
.gallery-nav {
  padding: 1rem;
  img {
    width: 4rem;
    height: 4rem;
  }
}
</style>
