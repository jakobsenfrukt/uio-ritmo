<template>
  <div class="home" id="toc1">
    <transition name="fade" appear>
      <Hero
        video="/images/logo/logo-anim-white.mp4"
        heading="Annual Report 2018"
        subhead="RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion"
      />
    </transition>
    <transition name="fadeup" appear>
      <section class="text">
        <p>2018 was the year that RITMO went from idea to reality. Even though many things have changed since we first started planning RITMO in 2012, the core people, the main ideas, and the excitement of being part of something quite unique, is still there!</p>
        <p>One of the things we are most proud of, is the truly interdisciplinary nature of RITMO. Everyone is talking about the need to work across disciplines, but not so many really try to do this in practice. As Centre Directors we spent a lot of time in 2018 on building a solid administrative and organizational platform for a centre that spans three departments in three faculties. We are grateful for the support we have received from the University of Oslo throughout this process, and we believe that the establishment of RITMO has helped pave the way for future interdisciplinary initiatives.</p>
        <p>The most important part of RITMO is the people working here. Many people moved from their host departments to RITMO in August 2018, and soon after we welcomed the first group of new recruits as they arrived in September. It was fantastic to see our premises change from a construction site into a buzzing working environment in just a few months.</p>
        <p>2018 was the year of change, the year that RITMO came into being. Here we present some highlights from the year, in time, rhythm, and motion.</p>
        <p class="quoteby">Anne Danielsen and Alexander Refsum Jensenius</p>
      </section>
    </transition>
    <Figure
      image="https://www.hf.uio.no/ritmo/english/research/time/colourbox18441910.jpg"
      alt="Bevegelse i dans"
      size="full"
    />
    <section id="toc2" class="text item">
      <h2>RITMO at a Glance</h2>
      <p>Rhythm is omnipresent in human life, as we walk, talk, dance and play; as we tell stories about our past; and as we predict the future. Rhythm is also central to human biology, from the oscillations of our nervous system to our heartbeats, breathing patterns and longer chronobiological cycles. As such, it is a key aspect of human action and perception that is in complex interplay with the various cultural, biological and mechanical rhythms of the world.</p>
      <p>RITMO undertakes research on rhythm in human action and perception, using music, motion and audio-visual media as empirical points of departure. Our core idea is that the human ability to experience the world and our actions as rhythmic, points to basic perceptual and cognitive mechanisms that are in themselves rhythmic in nature. <strong>The vision of RITMO</strong> is to understand more about these mechanisms, and through this generate new knowledge about the ways in which humans structure and understand the temporal dimensions of their life.</p>
      <p>The centre is interdisciplinary and combines perspectives and methods from music and media studies, philosophy and aesthetics, cognitive neuroscience, and informatics, using state-of-the-art technologies for motion capture, neuroimaging, pupillometry and robotics.</p>
    </section>
    <Figure
      image="/images/infographics/RITMO-Bobler.png"
      alt="Bildet viser no greier"
      size="column"
    />
    <section class="text item">
      <h3>Rythm</h3>
    </section>
    <section class="text item">
      <h3>Time</h3>
    </section>
    <section class="text item">
      <h3>Motion</h3>
    </section>
    <section id="toc3" class="text item">
      <h2>RITMO's Research Priorities</h2>
    </section>
    <Figure
      image="/images/infographics/RITMO-Matrise.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <section id="toc4" class="text item">
      <h2>RITMO in Numbers</h2>
    </section>
    <Figure
      image="/images/infographics/RITMO-Results.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <section id="toc5" class="text item">
      <h2>RITMO Highlights</h2>
    </section>
    <section id="toc6" class="text item">
      <h2>RITMO Stories</h2>
    </section>
    <Video
      video="/images/logo/logo-anim-white.mp4"
      size="column"
    />
    <section id="toc7" class="text item">
      <h2>RITMO Seminar Series</h2>
    </section>
    <section id="toc8" class="text item">
      <h2>RITMO Behind the Scenes</h2>
    </section>
    <section id="toc9" class="text item">
      <h2>RITMO's Profile</h2>
    </section>
    <section id="toc10" class="text item">
      <h2>Awards</h2>
    </section>
    <Figure
      image="https://www.hf.uio.no/ritmo/english/news-and-events/events/conferences/2018/ritmo-largo/photos/annica-thomson/3d9a5031.jpg"
      alt="The beautiful people of RITMO together on a stage"
      size="full"
    />
    <section id="toc11" class="text item">
      <h2>RITMO People</h2>
    </section>
    <Figure
      image="/images/infographics/RITMO-People-kjonn.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <section id="toc12" class="text item">
      <h2>International</h2>
    </section>
    <Figure
      image="/images/infographics/RITMO-Partners-land.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <Figure
      image="/images/infographics/RITMO-People-land.svg"
      alt="Bildet viser no greier"
      size="column"
    />
    <PersonList />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Video from '@/components/Video.vue'
import Figure from '@/components/Figure.vue'
import PersonList from '@/components/PersonList.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Video,
    Figure,
    PersonList
  }
}
</script>

