<template>
  <div id="app">
    <header id="header" class="site-header">
      <div class="logo"><img src="/uio-logo.svg" /></div>
      <nav class="site-nav">
        <div class="menu" :class="{ visible: showmenu }" id="main-menu">
          <ul>
            <!--<li><router-link to="/">Home</router-link></li>-->
            <h3>Annual Report 2018</h3>
            <span class="subhead">RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion</span>
            <li><a href="#" id="toc1-link" class="toc-link-active" v-scroll-to="{ el: '#toc1', onStart: togglemenu }">Intro</a></li>
            <li><a href="#" id="toc2-link" v-scroll-to="{ el: '#toc2', onStart: togglemenu }">RITMO at a Glance</a></li>
            <li><a href="#" id="toc3-link" v-scroll-to="{ el: '#toc3', onStart: togglemenu }">RITMO's Research Priorities</a></li>
            <li><a href="#" id="toc4-link" v-scroll-to="{ el: '#toc4', onStart: togglemenu }">RITMO in Numbers</a></li>
            <li><a href="#" id="toc5-link" v-scroll-to="{ el: '#toc5', onStart: togglemenu }">RITMO Highlights</a></li>
            <li><a href="#" id="toc6-link" v-scroll-to="{ el: '#toc6', onStart: togglemenu }">RITMO Stories</a></li>
            <li><a href="#" id="toc7-link" v-scroll-to="{ el: '#toc7', onStart: togglemenu }">RITMO Seminar Series</a></li>
            <li><a href="#" id="toc8-link" v-scroll-to="{ el: '#toc8', onStart: togglemenu }">RITMO Behind the Scenes</a></li>
            <li><a href="#" id="toc9-link" v-scroll-to="{ el: '#toc9', onStart: togglemenu }">RITMO's profile</a></li>
            <li><a href="#" id="toc10-link" v-scroll-to="{ el: '#toc10', onStart: togglemenu }">Awards</a></li>
            <li><a href="#" id="toc11-link" v-scroll-to="'#toc11'">RITMO People</a></li>
          </ul>
        </div>
        <div class="menu-toggle" :class="{ open: showmenu }" @click="togglemenu()">
          <div class="burger-wrapper">
            <div class="burger"></div>
          </div>
        </div>
      </nav>
    </header>
    <main class="site-main">
      <router-view/>
    </main>
    <footer class="site-footer">
      <div class="flex">
        <div>
          <a href="https://www.hf.uio.no/ritmo/english">
            RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion
          </a>
        </div>
        <div>
          <a href="https://uio.no">
            <img src="/uio-full.png" />
          </a>
        </div>
        <div>
          <p>
            Ansvarlig redaktør:<br />
            <a href="#">Navn Navnesen</a>
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import Vue from 'vue';
import VueScrollTo from 'vue-scrollto';

Vue.use(VueScrollTo)

export default {
  data: function() {
    return {
      showmenu: false
    }
  },
  methods: {
    togglemenu: function() {
      this.showmenu = !this.showmenu;
    },
    handleScroll: function() {
      this.fadeIn();
      this.updateMenu();
    },
    fadeIn: function() {
      const items = document.querySelectorAll('.item');
      for (const item of items) {
        if (item.getBoundingClientRect().top <= window.innerHeight * 0.8 && item.getBoundingClientRect().top > 0) {
          item.classList.add('inview');
        }
      }
    },
    updateMenu() {
      const chapters = document.querySelectorAll('.toc');
      for (const chapter of chapters) {
        if (chapter.getBoundingClientRect().top <= window.innerHeight * 0.5 || chapter.getBoundingClientRect().bottom < window.innerHeight * 0.5) {
          document.querySelector('.toc-inview').classList.remove('toc-inview');
          chapter.classList.add('toc-inview');
          const chapterId = chapter.getAttribute('id');
          const menu = document.querySelectorAll('#main-menu ul li a');
          for (const menuItem of menu) {
            if (menuItem.id === chapterId + '-link') {
              document.querySelector('.toc-link-active').classList.remove('toc-link-active');
              menuItem.classList.add('toc-link-active');
            }
          }
        }
      }
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll)
    this.updateMenu();
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="scss">
@import 'css/main.scss';

.logo {
  padding-right: 0.6rem;
  position: relative;
}

.site-header {
  width: 100%;
  background: $color-theme-dark;
  color: $color-white;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 1rem;

  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: 200;


  a {
    color: $color-white;
  }

  .menu-toggle {
    display: block;

    cursor: pointer;
    position: absolute;
    top: 1.5rem;
    right: 1rem;

    transition-timing-function: linear;
    transition-duration: .15s;
    transition-property: opacity,filter;

    .burger-wrapper {
      position: relative;
      width: 1.6rem;
      height: 1.6rem;
      display: block;

      .burger {
        transition-timing-function: cubic-bezier(.55,.055,.675,.19);
        transition-duration: 75ms;
        position: absolute;
        width: 1.8rem;
        height: 4px;
        transition-timing-function: ease;
        transition-duration: 0.2s;
        transition-property: transform;
        border-radius: 4px;
        background: $color-white;

        &:before, &:after {
          display: block;
          content: "";
          position: absolute;
          width: 1.8rem;
          height: 4px;
          transition-timing-function: ease;
          transition-duration: 0.2s;
          transition-property: transform;
          border-radius: 4px;
          background: $color-white;
        }
        &:before {
          transition: top 75ms ease .12s,opacity 75ms ease;
          top: -10px;
        }
        &:after {
          transition: bottom 75ms ease .12s,transform 75ms cubic-bezier(.55,.055,.675,.19);
          bottom: -10px;
        }
      }
    }

    &.open {
      .burger-wrapper {
        .burger {
          transition-delay: 0.06s;
          transition-timing-function: cubic-bezier(.215,.61,.355,1);
          transform: rotate(45deg);
          background: $color-white;

          &:before {
            top: 0;
            transition: top 75ms ease,opacity 75ms ease 0.16s;
            opacity: 0;
          }
          &:after {
            bottom: 0;
            transition: bottom 75ms ease,transform 75ms cubic-bezier(.215,.61,.355,1) .12s;
            transform: rotate(-90deg);
          }
        }
      }
    }

    &:hover {
      .burger-wrapper .burger {
          background: $color-red;
          &:before, &:after {
            background: $color-red;
          }
        }
    }
  }

  .menu {
    position: fixed;
    top: 3rem;
    right: 0;
    bottom: 0;
    overflow-y: auto;
    z-index: 2100;
    padding: 1rem;
    width: $width-xs;
    color: $color-white;
    background: $color-theme-dark;

    transform: translateX(100vw);
    transition: transform .3s ease-in-out;

    &.visible {
      transform: translateX(0);
    }

    @media (max-width: $media-s) {
      width: 100%;
    }

    h3 {
      margin: 0;
      font-size: 2rem;
      color: inherit;
    }
    .subhead {
      font-size: $font-s;
      line-height: 1.2;
      display: block;
      margin: 0.5rem 0 2rem;
      @media (max-width: $media-s) {
        font-size: 1rem;
      }
    }

    ul {
      list-style: none;
      font-size: 1.2rem;
      font-family: $sans-serif;

      @media (max-width: $media-s) {
        max-width: none;
        width: 100%;
        padding: 0;
      }
    }

    li {
      margin-left: 0.2rem;
      
      ul {
        margin-top: 0.6rem;
        font-size: 1rem;
      }
    }

    a {
      color: $color-white;
      text-decoration: none;
      &:before {
        content: " ";
        display: inline-block;
        width: 0.4rem;
        height: 0.4rem;
        vertical-align: middle;
        background: $color-turquoise;
        border-radius: 0.4rem;
        margin-right: 0.6rem;
      }
      &.toc-link-active {
        &:before {
          background: $color-red;
        }
      }
    }

    /* ritmo specific style */
    a:before {
      transition: width .1s ease-in-out;
    }
    a:hover {
      text-decoration: none;
      &:before {
        width: 1rem;
        height: 0.4rem;
        border-radius: 0.4rem;
        margin-right: 0.6rem;
        transition: width .1s ease-in-out;
      }
    }
  }
}

.site-footer {
  width: 100%;
  padding: 5rem 1rem;
  background: $color-theme-dark;
  color: $color-white;

  text-align: center;
  font-family: $serif;

  .flex {
    width: $width-xl;
    max-width: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;

    div {
      width: 25%;
    }
  }

  p {
    line-height: 1.2;
    margin: 0 auto;
  }

  img {
    vertical-align: middle;
    padding: 0.5rem;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  @media (max-width: $media-m) {
    .flex {
      display: block;

      div {
        width: 100%;
        margin-bottom: 1rem;
      }
    }
  }
}
</style>
