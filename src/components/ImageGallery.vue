<template>
  <section class="gallery">
    <div class="figure item">
      <figure>
        <img :src="images[currentImage].url" />
        <div class="caption-wrapper">
          <figcaption>
            {{ images[currentImage].caption }}
            <span class="photoby">Foto: Svein Stølen</span>
          </figcaption>
        </div>
      </figure>
    </div>
    <nav class="gallery-nav">
      <img v-for="(image, index) in images" :key="`image-${index}`" :src="image.url" @click="changeImage(index)" />
    </nav>
    <nav class="pagination">
      <div class="previous" @click="currentImage > 0 ? currentImage-- : null">prev</div>
      <div class="next" @click="currentImage < images.length-1 ? currentImage++ : null">next</div>
    </nav>
  </section>
</template>

<script>
export default {
  name: 'ImageGallery',
  props: {
    images: Array
  },
  data: function() {
    return {
      currentImage: 0
    }
  },
  methods: {
    changeImage: function(index) {
      this.currentImage = index;
    }
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
    width: $width-s;
    margin: 0;
    position: absolute;
    max-width: 90%;
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
    margin-right: 1rem;
    &:last-child {
      margin-right: 0;
    }
    cursor: pointer;
    &:hover {
      opacity: 0.6;
    }
  }
}

/* RITMO SPECIFIC STYLE */

div {
  figcaption {
    padding: 1rem 3rem 1rem 2rem;
    border-radius: 5rem;
    border-top-left-radius: 0;
    border-bottom-left-radius: 0;
    left: -1rem;
    bottom: 1rem;
    background-color: $color-white;
    color: $color-blue;
  }
}

</style>
