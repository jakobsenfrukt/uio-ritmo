<template>
  <div id="app">
    <header id="header" class="site-header">
      <div class="logo">UiO</div>
      <nav class="site-nav">
        <div class="menu" :class="{ visible: showmenu }" id="main-menu">
          <ul>
            <!--<li><router-link to="/">Home</router-link></li>-->
            <h3>Annual Report 2018</h3>
            <span class="subhead">RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion</span>
            <li><a href="#" v-scroll-to="{ el: '#toc1', onStart: togglemenu }">Intro</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc2', onStart: togglemenu }">RITMO at a Glance</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc3', onStart: togglemenu }">RITMO's Research Priorities</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc4', onStart: togglemenu }">RITMO in Numbers</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc5', onStart: togglemenu }">RITMO Highlights</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc6', onStart: togglemenu }">RITMO Stories</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc7', onStart: togglemenu }">RITMO Seminar Series</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc8', onStart: togglemenu }">RITMO Behind the Scenes</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc9', onStart: togglemenu }">RITMO's profile</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc10', onStart: togglemenu }">Awards</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc11', onStart: togglemenu }">Innovation Prize</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc12', onStart: togglemenu }">Adacemy Membership</a></li>
            <li><a href="#" v-scroll-to="{ el: '#toc13', onStart: togglemenu }">EUA Committee</a></li>
            <li><a href="#" v-scroll-to="'#toc14'">RITMO People</a></li>
            <li><a href="#" v-scroll-to="'#toc15'">International</a></li>
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
      <a href="#">Gå til uio.no</a>
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
      const items = document.querySelectorAll('.item');
      for (const item of items) {
        if (item.getBoundingClientRect().top <= window.innerHeight * 0.8 && item.getBoundingClientRect().top > 0) {
          item.classList.add('inview');
        }
      }
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="scss">
@import 'css/main.scss';

.logo {
  font-family: $serif;
  padding-right: 0.6rem;
  position: relative;
  &:before, &:after {
    content: " ";
    display: block;
    width: 0.32rem;
    height: 0.32rem;
    border-radius: 50%;
    background: $color-red;
    position: absolute;
    top: 0.24rem;
    right: 0;
  }
  &:after {
    top: 0.7rem;
  }
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
        background-color: #fff;

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
          background-color: #fff;
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
          transition-delay: 0.16s;
          transition-timing-function: cubic-bezier(.215,.61,.355,1);
          transform: rotate(45deg);
          background-color: #fff;

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
  }

  .menu {
    position: fixed;
    top: 3rem;
    right: 0;
    bottom: 0;
    overflow-y: auto;
    z-index: 100;
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
    }
    .subhead {
      font-size: $font-s;
      line-height: 1.2;
      display: block;
      margin: 0.5rem 0 2rem;
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
      margin-left: 1rem;
      &:before {
        content: " ";
        display: inline-block;
        width: 0.4rem;
        height: 0.4rem;
        background: $color-red;
        border-radius: 50%;
        margin-right: 0.6rem;
      }
      

      ul {
        margin-top: 0.6rem;
        font-size: 1rem;
      }
    }

    a {
      color: $color-white;
      &:hover {
        text-decoration: underline;
      }
    }
  }
}

.site-footer {
  width: 100%;
  padding: 8rem 1rem 4rem;
  background: $color-theme-dark;
  color: $color-white;

  text-align: center;

  a {
    color: inherit;
    text-decoration: underline;
  }
}
</style>
