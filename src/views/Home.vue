<template>
  <div class="home">
    <transition name="fade" appear>
      <Hero
        video="/images/logo/logo-anim-white.mp4"
        heading="Annual Report 2018"
        subhead="RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion"
      />
    </transition>
    <transition name="fadeup" appear>
      <section id="part1" class="text">
        <p>2018 was the year that RITMO went from idea to reality. Even though many things have changed since we first started planning RITMO in 2012, the core people, the main ideas, and the excitement of being part of something quite unique, is still there!</p>
      </section>
    </transition>
    <Figure
      image="/images/infographics/RITMO-Bobler.png"
      alt="Bildet viser no greier"
      size="column"
    />
    <section id="part1" class="text item">
      <h2>Overskrift H2</h2>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.</p>
    </section>
    <Figure
      image="/images/infographics/RITMO-Matrise.svg"
      alt="Bildet viser no greier"
      size="small"
    />
    <Figure
      image="/images/infographics/RITMO-Partners-land.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <Figure
      image="/images/infographics/RITMO-People-kjonn.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <Figure
      image="/images/infographics/RITMO-People-land.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <Figure
      image="/images/infographics/RITMO-Results.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <Video
      video="/images/logo/logo-anim-white.mp4"
      size="column"
    />
    <section id="end" class="text item background people">
      <h3>Ansatte</h3>
      <ul>
        <li>
          <img src="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg" />
          <h4 class="name">Navn Navnesen</h4>
          <p class="bio">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</p>
        </li>
        <li>
          <img src="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg" />
          <h4 class="name">Navn Navnesen</h4>
          <p class="bio">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</p>
        </li>
        <li>
          <img src="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg" />
          <h4 class="name">Navn Navnesen</h4>
          <p class="bio">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Video from '@/components/Video.vue'
import Figure from '@/components/Figure.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Video,
    Figure
  }
}
</script>

