<template>
  <section class="gallery item">
    <div class="figure">
      <figure>
        <img :src="images[currentImage].url" />
        <div v-if="images[currentImage].caption" class="caption-wrapper">
          <figcaption>
            {{ images[currentImage].caption }}
            <span v-if="images[currentImage].credit" class="credit">{{ images[currentImage].credit }}</span>
          </figcaption>
        </div>
      </figure>
    </div>
    <nav class="gallery-nav">
      <img v-for="(image, index) in images" :key="`image-${index}`" :src="image.url" @click="changeImage(index)" :class="currentImage === index ? 'active' : null" />
    </nav>
    <nav class="pagination">
      <div class="pagination-button previous" @click="currentImage > 0 ? currentImage-- : null"><div class="arrow"></div></div>
      <div class="pagination-button next" @click="currentImage < images.length-1 ? currentImage++ : null"><div class="arrow"></div></div>
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
  background: $color-white;
  margin-bottom: 4rem;
  position: relative;
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
    left: 0; right: 0; bottom: 1rem;
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
  .credit {
    font-size: $font-xs;
    display: block;
    font-style: italic;
    text-align: right;
    font-family: $sans-serif;
  }
}
.gallery-nav {
  padding: 0 1rem;
  img {
    width: 4rem;
    height: 4rem;
    margin: 0.5rem;
    &:last-child {
      margin-right: 0;
    }
    &:first-child {
      margin-left: 0;
    }
    cursor: pointer;
    &:hover {
      opacity: 0.6;
    }
    &.active {
      box-shadow: 0 0 0 0.2rem $color-turquoise;
    }
  }
}

.pagination {
  &-button {
    position: absolute;
    z-index: 2000;
    top: calc(50% - 3rem);
    width: 3rem;
    height: 3rem;
    background: $color-turquoise;
    border-radius: 50%;
    cursor: pointer;
    &:hover {
      background: $color-red;
    }
    .arrow {
      width: 18px;
      height: 20px;
      border-width: 4px 4px 0 0;
      border-style: solid;
      margin: 1rem;
      border-radius: 0 2px 0 0;
      &:before, &:after {
        content: "";
        border-radius: 2px;
        position: absolute;
      }
      &:before {
        right: 0;
        top: -3px;
        width: 23px;
        height: 4px;
        -webkit-transform: rotate(-45deg);
        transform: rotate(-45deg);
        -webkit-transform-origin: right top;
        transform-origin: right top;
        box-shadow: inset 0 0 0 32px;
      }
      &:after {
        width: 4px;
        height: 4px;
        left: -2px;
        top: -4px;
        box-shadow: inset 0 0 0 32px, 16px 17px;
      }
    }
  }
  .next {
    right: 0.5rem;
    transform: rotate(45deg);

  }
  .previous {
    left: 0.5rem;
    transform: rotate(-135deg);
  }
}

/* RITMO SPECIFIC STYLE */

div {
  figcaption {
    padding: 1rem 1rem 1rem 2rem;
    border-radius: 1rem;
    border-top-left-radius: 0;
    border-bottom-left-radius: 0;
    left: -1rem;
    bottom: 1rem;
    background-color: $color-black;
    color: $color-white;
    font-family: $serif;
  }
}

</style>
