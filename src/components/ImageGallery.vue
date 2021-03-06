<template>
  <section class="gallery item">
    <div class="figure" v-touch:swipe.left="previousImage" v-touch:swipe.right="nextImage">
      <figure>
        <img :src="images[currentImage].url" class="main-image" />
        <div v-if="images[currentImage].caption" class="caption-wrapper">
          <figcaption>
            {{ images[currentImage].caption }}
            <span v-if="images[currentImage].credit" class="credit">{{ images[currentImage].credit }}</span>
          </figcaption>
        </div>
      </figure>
    </div>
    <nav class="gallery-nav">
      <div class="pagination-button previous"><img class="arrow" src="/images/arrow-left.svg" /></div>
      <div class="inner">
        <img v-for="(image, index) in images" :key="`image-${index}`" :src="image.url" @click="changeImage(index)" :class="currentImage === index ? 'active' : null" class="nav-image" />
      </div>
      <div class="pagination-button next"><img class="arrow" src="/images/arrow-right.svg" /></div>
    </nav>
    <nav class="pagination">
      <div class="pagination-button previous" @click="currentImage > 0 ? currentImage-- : null"><img class="arrow" src="/images/arrow-left.svg" /></div>
      <div class="pagination-button next" @click="currentImage < images.length-1 ? currentImage++ : null"><img class="arrow" src="/images/arrow-right.svg" /></div>
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
    },
    nextImage: function() {
      this.currentImage > 0 ? this.currentImage++ : null
    },
    previousImage: function() {
      this.currentImage > 0 ? this.currentImage-- : null
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';
.gallery {
  padding: 0;
  background: $color-white;
  margin-bottom: 8rem;
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
    object-fit: contain;
    z-index: 1;
  }

  .main-image, .nav-image {
    background: $color-black;
  }

  .caption-wrapper {
    position: absolute;
    top: 1rem;
    left: 0; right: 0; bottom: 1rem;
    z-index: 2;
    display: flex;
    align-items: flex-end;
    justify-content: center;
  }

  figcaption {
    padding: 0.6rem 1rem;
    width: $width-s;
    max-width: 90%;
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
  width: 100%;
  max-width: 100%;
  height: 5rem;
  overflow: hidden;
  .inner {
    padding: 0 4rem;
    display: flex;
    overflow-x: scroll;
    padding-bottom: 17px;
  }
  img {
    object-fit: cover;
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
      box-shadow: 0 0 0 0.2rem $color-turquoise;
    }
    &.active {
      box-shadow: 0 0 0 0.2rem $color-turquoise;
    }
  }
  .pagination-button {
    background: $color-white;
    bottom: 1.6rem;
    top: auto;
    &:hover {
      background: $color-white;
      img {
        box-shadow: none;
      }
    }
  }
}

.pagination {
  &-button {
    position: absolute;
    z-index: 2;
    top: calc(50% - 2.6rem);
    width: 2.6rem;
    height: 2.6rem;
    background: $color-turquoise;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background .2s ease-in-out;
    &:hover {
      background: $color-red;
    }
    .arrow {
      width: 1rem;
      height: 1rem;
    }
    &.next {
      right: 0.5rem;
    }
    &.previous {
      left: 0.5rem;
    }
  }
}

@media (max-width: $width-m) {
  img {
    object-position: center;
  }
  .pagination {
    &-button {
      width: 2rem;
      height: 2rem;
    }
  }
}

/* RITMO SPECIFIC STYLE */

div {
  figcaption {
    padding: 1rem;
    background-color: $color-white;
    color: $color-black;
    font-family: $serif;
  }
}

</style>
