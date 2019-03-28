<template>
  <div class="home toc toc-inview" id="toc1">
    <transition name="fade" appear>
      <Hero
        video="/images/logo/logo-anim-white.mp4"
        heading="Annual Report 2018"
        subhead="RITMO - Centre for Interdisciplinary Studies in Rhythm, Time and Motion"
      />
    </transition>
    <transition name="fadeup" appear>
      <section class="text">
        <p class="lead">2018 was the year that RITMO went from idea to reality. Even though many things have changed since we first started planning RITMO in 2012, the core people, the main ideas, and the excitement of being part of something quite unique, is still there!</p>
        <p>One of the things we are most proud of, is the truly interdisciplinary nature of RITMO. Everyone is talking about the need to work across disciplines, but not so many really try to do this in practice. As Centre Directors we spent a lot of time in 2018 on building a solid administrative and organizational platform for a centre that spans three departments in three faculties. We are grateful for the support we have received from the University of Oslo throughout this process, and we believe that the establishment of RITMO has helped pave the way for future interdisciplinary initiatives.</p>
        <p>The most important part of RITMO is the people working here. Many people moved from their host departments to RITMO in August 2018, and soon after we welcomed the first group of new recruits as they arrived in September. It was fantastic to see our premises change from a construction site into a buzzing working environment in just a few months.</p>
        <p>2018 was the year of change, the year that RITMO came into being. Here we present some highlights from the year, in time, rhythm, and motion.</p>
        <p class="quoteby">Anne Danielsen and Alexander Refsum Jensenius</p>
      </section>
    </transition>
    <Figure
      image="https://www.hf.uio.no/ritmo/english/about/yearly-report/images/danielsen-og-jensenius.jpg"
      alt="Anne og Alexander"
      size="column"
    />
    <Figure
      image="https://www.hf.uio.no/ritmo/english/research/time/colourbox18441910.jpg"
      alt="Bevegelse i dans"
      size="full"
    />
    <section id="toc2" class="toc text item">
      <h2 class="section-heading">RITMO at a Glance</h2>
      <p>Rhythm is omnipresent in human life, as we walk, talk, dance and play; as we tell stories about our past; and as we predict the future. Rhythm is also central to human biology, from the oscillations of our nervous system to our heartbeats, breathing patterns and longer chronobiological cycles. As such, it is a key aspect of human action and perception that is in complex interplay with the various cultural, biological and mechanical rhythms of the world.</p>
      <p>RITMO undertakes research on rhythm in human action and perception, using music, motion and audio-visual media as empirical points of departure. Our core idea is that the human ability to experience the world and our actions as rhythmic, points to basic perceptual and cognitive mechanisms that are in themselves rhythmic in nature. <strong>The vision of RITMO</strong> is to understand more about these mechanisms, and through this generate new knowledge about the ways in which humans structure and understand the temporal dimensions of their life.</p>
      <p>The centre is interdisciplinary and combines perspectives and methods from music and media studies, philosophy and aesthetics, cognitive neuroscience, and informatics, using state-of-the-art technologies for motion capture, neuroimaging, pupillometry and robotics.</p>
    </section>
    <Figure
      image="/images/infographics/RITMO-Bobler.png"
      alt="Bildet viser no greier"
      size="column"
    />
    <FixedGallery :media="gallery7" />
    <section id="toc3" class="toc text item">
      <h2 class="section-heading">RITMO's Research Priorities</h2>
      <p class="lead">In addition to RITMO's organizational clusters and operational research groups described above, we also have four research priorities that influence and guides all the other activities:</p>
    </section>
    <TwoColumn />
    <section id="toc4" class="toc text item">
      <h2 class="section-heading">RITMO in Numbers</h2>
    </section>
    <FixedGallery :media="gallery6" />
    <section id="toc5" class="toc text item">
      <h2 class="section-heading">RITMO Highlights</h2>
      <p class="lead">At a centre with more than 40 employees, there are always numerous things happening. In 2018 we were particularly proud of three things.</p>
    </section>
    <section class="text item">
      <h3>Moving in</h3>
    </section>
    <ImageGallery :images="gallery1" />
    <section class="text item">
      <h3>RITMO Largo</h3>
    </section>
    <ImageGallery :images="gallery2" />
    <section class="text item">
      <h3>RITMO International Motion Capture Workshop</h3>
      <p>A workshop for exploring advanced methods for capturing and analysing human music-related motion. <a href="https://www.hf.uio.no/ritmo/english/news-and-events/events/conferences/2018/motion-capture/index.html">Read more</a></p>
    </section>
    <ImageGallery :images="gallery3" />
    <section id="toc6" class="toc text item">
      <h2 class="section-heading">RITMO Stories</h2>
      <p class="lead">A project is always more than what you can read from a project page. Hear some of RITMO's researchers present their own research.</p>
    </section>
    <FixedGallery :media="gallery8" />
    <section id="toc7" class="toc text item background">
      <h2 class="section-heading">RITMO Seminar Series</h2>
      <p class="lead">In 2018 we started up the RITMO Seminar Series as a venue for presenting world-leading scholars from around the world. These events are open to the public, and have attracted participants from all over the Oslo area.</p>
      <MultiColumn :blocks="blocks2" />
    </section>
    <section id="toc8" class="toc text item">
      <h2 class="section-heading">RITMO Behind the Scenes</h2>
      <p class="lead">To the people working at RITMO, the Centre is so much more than just a working space. Even though the everyday life at the center evolves around topics of research and work, the treshold for socialising and laughing are low, which creates a warm nergetic environment for the staff.</p>
    </section>
    <ImageGallery :images="gallery4" />
    <section id="toc9" class="toc text item">
      <h2 class="section-heading">RITMO's Profile</h2>
      <p class="lead">It was clear from the start that RITMO could not only have a static, visual profile. After all, RITMO is about time, rhythm, and motion, and we wanted this to come through in our physical and digital appearance.</p>
      <p>The solution was to engage in a creative process with the design company Anagram and the composer Jon Balke. The end result is a sonic-visual profile that captures some of the creative spirit of RITMO, and that can be reconfigured endlessly.</p>
    </section>
    <FixedGallery :media="gallery5" />
    <section id="toc10" class="toc text item background">
      <h2 class="section-heading">Awards</h2>
      <MultiColumn :blocks="blocks1" />
    </section>
    <section id="toc11" class="toc text item">
      <h2 class="section-heading">RITMO People</h2>
      <p class="lead">The people are the most important part of RITMO.</p>
    </section>
    <Figure
      image="https://www.hf.uio.no/ritmo/english/news-and-events/events/conferences/2018/ritmo-largo/photos/annica-thomson/3d9a5031.jpg"
      alt="The beautiful people of RITMO together on a stage"
      size="full"
    />
    <section class="text item">
      <h3>Scientific Advisory Board</h3>
      <p>The members of RITMO's Scientific Advisory Board are highly acclaimed researchers within their respective fields. The Board is vital to providing feedback on on-going and future research, and its members have been carefully chosen to support the different parts of RITMO.</p>
    </section>
    <PersonList :people="people1" />
    <PersonList :people="people2" heading="Steering Committee" />
    <LogoList />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/Hero.vue'
import Figure from '@/components/Figure.vue'
import PersonList from '@/components/PersonList.vue'
import ImageGallery from '@/components/ImageGallery.vue'
import TwoColumn from '@/components/TwoColumn.vue'
import FixedGallery from '@/components/FixedGallery.vue'
import MultiColumn from '@/components/MultiColumn.vue'
import LogoList from '@/components/LogoList.vue'

export default {
  name: 'home',
  components: {
    Hero,
    Figure,
    PersonList,
    ImageGallery,
    TwoColumn,
    FixedGallery,
    MultiColumn,
    LogoList
  },
  data: function() {
    return {
      gallery1: [
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3010.jpg',
          caption: 'In August RITMO\'s staff moved into their new premises in Harald Schjelderups hus. Here Ragnhild Brøvig-Hanssen is filling the shelves in her new office.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3071.jpg',
          caption: 'From before, RITMO\'s staff was located at three different departments and in three different buildings at the University of Oslo. The moving load was impressive! Bruno Laeng filled quite a few boxes.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3075.jpg',
          caption: 'It was great to finally be co-located and working together in the same building. Centre director Anne Danielsen is unpacking one of the many boxes.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3103.jpg',
          caption: 'The premises were refurbished during the spring and summer before RITMO could move in. This is going to be a shared office for PhDs and Postdocs.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3108.jpg',
          caption: 'Once in a while we were a bit worried whether or not they would be finished in time for us to move in.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3122.jpg',
          caption: 'Moving is hard work. Coffee and cinnamon buns were important to keep the spirit up!',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a3171.jpg',
          caption: 'The RITMO staff had quite a job both packing and unpacking. Bruno Laeng and Ragnhild Brøvig-Hanssen are getting things in order.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/moving-in/3d9a2928.jpg',
          caption: 'Moving and working! Kristian Nymoen tries to get some work done during the moving process.',
          credit: 'Photo: Annica Thomsson'
        }
      ],
      gallery2: [
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5048.jpg',
          caption: 'Liv Furuberg from the Research Council of Norway handed over the Centre of Excellence plaque to director Anne Danielsen.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5149.jpg',
          caption: 'Members of RITMO\'s Scientific Advisory Board and Faculty discussed the highly relevant subject of working across disciplinary borders.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5171.jpg',
          caption: 'After the opening, everyone was invited to the grand reception.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5219.jpg',
          caption: 'In the evening the fun and celebration continued. MusicLab 3, organised by the University library in cooperation with RITMO, explored the phenomenon of rhythm - in music and in the body - all within MusicLab’s unique blend of research and edutainment. Solveig Isis Sørbø and Sophie Charlotte Barth wished everyone welcome.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5297.jpg',
          caption: 'After the music-dance performance, rhythm was discussed by Professor Justin London, RITMO\'s director Anne Danielsen, Dancer-illustrator Katja Schia and DJ Filip Abramczyk. RITMO\'s deputy director, Alexander Refsum Jensenius, lead the discussion.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/5r0a9325.jpg',
          caption: 'Guests from all over the world joined in on the opening event.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a4995.jpg',
          caption: 'Batagraf set the tone for the official opening of RITMO.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5247.jpg',
          caption: 'Coding in action! Some of our researchers did live coding of movements to music. Here presented by Cagri Erdem and Qichao Lan analysing Katja Schias\' dance.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5207.jpg',
          caption: 'Good times! After months of planning the opening, a feast was welcome.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a4973.jpg',
          caption: 'UiO Rector Svein Stølen talks to RITMO Centre Directors Anne Danielsen and Alexander Refsum Jensenius.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/largo/3d9a5032.jpg',
          caption: 'All our staff was invited to share the stage for the opening.',
          credit: 'Photo: Annica Thomsson'
        }
      ],
      gallery3: [
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/3d9a4770.jpg',
          caption: 'In connection with RITMO\'s official opening, the centre organized a international workshop on music-related motion capture 12-14 November. RITMO\'s administration is ready to welcome more than 50 experts from all over the world.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/3d9a4771.jpg',
          caption: 'The program included keynotes by Marcelo M. Wanderley, Marc Leman and Peter Vuust, as well as panel discussions, hands-on sessions and toolbox tutorials.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/3d9a4833.jpg',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/5r0a9015.jpg',
          caption: 'The workshop also included a tour of RITMO\'s lab facilities. Here Bruno Laeng is presenting the pupillometry lab.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/5r0a9034.jpg',
          caption: 'During the lunch break there was time for lively discussions and for getting to know colleagues from all over the world.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/5r0a9097.jpg',
          caption: 'There were hands-on sessions in the motion capture lab.',
          credit: 'Photo: Annica Thomsson'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/5r0a9134.jpg',
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/5r0a9140.jpg',
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/mocap/5r0a9189.jpg'
        }
      ],
      gallery4: [
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/social/engo.png'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/social/engo2.png'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/social/engo3.png'
        },
        {
          url: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/social/julebord2.jpg'
        }
      ],
      gallery5: [
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/ritmo-hovedmerke-290818.png',
          heading: 'The Visual Profile',
          quote: 'We have developed a visual mark/emblem based on the letter forms in the word RITMO, broken down to its smallest geometric constituents. The visual profile is a starting point consisting of flexible building blocks and some “rules“ for use, which can be varied indefinitely and generate new opinions, structures and constellations.',
          credit: 'Anagram'
        },
        {
          video: '/images/logo/logo-anim-white.mp4',
          heading: 'The Sonic Profile',
          quote: 'The sonic profile is designed to match RITMO\'s organic bodily understanding of rhythms to a more psychological approach, via social and cultural aspects. It was important for me to create something that is not tied up in a locked sense of pace or groove, but represents a rhythmic force and a course that could be experienced dramaturgically.',
          credit: 'Jon Balke, Batagraf'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/20181115_190400_320px.jpg',
          heading: 'The Dynamic Profile',
          quote: 'I was excited to be the first one to explore the re-configuration possibilities of the visual elements of RITMO\'s profile. The result, shown at RITMO Largo, was an interactive display of the visual elements projected on the floor. The elements reacted to the sound in the space. It was fascinating to see the elements come alive with people\'s talking and music playing, and I got many ideas for how to further develop the interaction.',
          credit: 'Julian Fuhrer, RITMO PhD student'
        },
      ],
      gallery6: [
        {
          video: '/images/infographics/RITMO-Results.mp4',
          heading: 'RITMO Publications',
          caption: 'RITMO\'s reserachers have published a number of scientific articles and book chapters in 2018. They have also given talks and presentations a large number of conferences around the world. The Centre\'s research results also include tool  boxes and apps, as well as several media contributions.',
          link: {
            url: '#',
            text: 'List of all RITMO publications'
          }
        },
        {
          video: '/images/infographics/RITMO-People-kjonn.mp4',
          heading: 'The People of RITMO',
          caption: 'RITMO consists of 61 people in total: 26 women and 34 men.'
        },
        {
          image: '/images/infographics/RITMO-People-land.svg',
          heading: 'The World at RITMO',
          caption: 'We are fortunate to have people from all over the world working at RITMO. Currently, we have people from: Argentina, Australia, Brazil, Columbia, Denmark, Finland, France, Greece, India, Italy, China, Mexico, Montenegro, Norway, Poland, Great Britain, Turkey, Germany, and USA.'
        },
        {
          image: '/images/infographics/RITMO-Partners-land.svg',
          heading: 'RITMO in the World',
          caption: 'Argentina, Belgium, Brazil, Canada, Switzerland, Germany, Denmark, Spain, Finland, France, United Kingdom, Israel, India, Iceland, Italy, Japan, Netherlands, Sweden, USA.'
        }
      ],
      gallery7: [
        {
          image: '/images/rythm.jpg',
          heading: 'Rythm',
          text: [
            'In the RHYTHM research cluster we investigate the basic structures and features of rhythmic phenomena as well as the links between these structures and features and the ways in which time is organized in human perception and cognition. We are also interested in why some rhythms are experienced as pleasurable and invite dance or other forms of body motion, whereas others do not.',
            'We investigate rhythm at various temporal scales, from micro-rhythmic relationships at the millisecond level to patterns of rhythms unfolding over several seconds. We are particularly interested in complex rhythms, rhythmic variation (micro-rhythm), rhythm across modalities (hearing, vision and body motion) and cultural variation. We use qualitative, behavioral and neurophysiological methods, often combining them to shed light on the same questions from different angles.',
            'Our aim is to understand how rhythm underpins our ability to structure past and predict future events, and to identify the perceptual and cognitive mechanisms underlying the experience and execution of rhythm.'
          ]
        },
        {
          image: '/images/time.jpg',
          heading: 'Time',
          text: [
            'The TIME research cluster addresses the ways in which rhythm impacts the structuring of temporal events beyond the ‘now’, that is, the extent to which rhythm plays a role in remembering and structuring longer time spans. We will also investigate the relationship between rhythm and the experience of fragmented time.',
            'A second priority is to investigate the temporality of experiences of pleasure and absorption, the fact that rhythm facilitates entrainment and synchronization, and the social dimensions of this aspect of rhythm. A related question is how philosophical, psychological, and historical explorations of time can be revisited through new interdisciplinary perspectives on the experience of rhythm.',
            'Our aim is to understand how rhythm underpins our ability to structure and remember large-scale formations of time, and to understand the related processes of pleasure and engagement.'
          ]
        },
        {
          image: '/images/motion.jpg',
          heading: 'Motion',
          text: [
            'The MOTION research cluster focuses on the analysis of human body rhythm and the synthesis of rhythms with machines. The aim is to understand more about the human body\'s internal and external rhythms and how rhythms can be used in interaction. It is also relevant to understand how music influences people\'s body motion, such as in dancing, but also when trying to stand still. Knowledge about the motion-inducing effects of music can then be used in the creation of interactive systems in which the music is controlled through the human body.',
            'The empirical work is done using various types of motion capture systems and physiological measurements. The analysis and synthesis parts also greatly involve computer-based analysis methods, and in particular different types of machine learning systems. The synthesis part includes both the creation of visual displays of motion (animations) and the creation and use of robots to create physical motion.',
            'The aim is to create basic knowledge that can be used in the development of advanced rhythmic human-robot interaction, such as in dancing.'
          ]
        }
      ],
      gallery8: [
        {
          video: '/images/logo/logo-anim-white.mp4',
          controls: true,
          heading: 'Et intervjuobjekt',
          caption: 'Dette er en liten tekst om hva du får se i filmen ved siden av, som introduserer intervjuobjektet og temaet han eller hun forsker på. Lorem ipsum dolor si amet og så videre.'
        },
        {
          video: '/images/logo/logo-anim-white.mp4',
          controls: true,
          heading: 'Et intervjuobjekt',
          caption: 'Dette er en liten tekst om hva du får se i filmen ved siden av, som introduserer intervjuobjektet og temaet han eller hun forsker på. Lorem ipsum dolor si amet og så videre.'
        },
        {
          video: '/images/logo/logo-anim-white.mp4',
          controls: true,
          heading: 'Et intervjuobjekt',
          caption: 'Dette er en liten tekst om hva du får se i filmen ved siden av, som introduserer intervjuobjektet og temaet han eller hun forsker på. Lorem ipsum dolor si amet og så videre.'
        },
        {
          video: '/images/logo/logo-anim-white.mp4',
          controls: true,
          heading: 'Et intervjuobjekt',
          caption: 'Dette er en liten tekst om hva du får se i filmen ved siden av, som introduserer intervjuobjektet og temaet han eller hun forsker på. Lorem ipsum dolor si amet og så videre.'
        }
      ],
      people1: [
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/georgina-born.jpg',
          name: 'Georgina Born',
          link: 'http://www.music.ox.ac.uk/about/people/academic-staff/university-lecturers-and-college-fellows/georgina-born/',
          bio: 'Professor of Music and Anthropology at the Faculty of Music, University of Oxford.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/nicholas-cook.jpg',
          name: 'Nicholas Cook',
          link: 'https://www.mus.cam.ac.uk/directory/nicholas-cook',
          bio: 'Professor of Music at the Faculty of Music, University of Cambridge.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/bilder/nikkidweb.jpg',
          name: 'Nicola Dibben',
          link: 'https://www.sheffield.ac.uk/music/staff/academic/ndibben/index',
          bio: 'Professor in the Department of Music, University of Sheffield.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/bilder/rebecca_fiebrink.jpg',
          name: 'Rebecca Fiebrink',
          link: 'https://www.doc.gold.ac.uk/~mas01rf/homepage/',
          bio: 'Senior Lecturer in Computing at Goldsmiths, University of London.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/bilder/robert_knight.jpg',
          name: 'Robert T. Knight',
          link: 'https://psychology.berkeley.edu/people/robert-t-knight',
          bio: 'Professor of Psychology and Neuroscience at Berkeley, University of California.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/serge-lacasse.jpg',
          name: 'Serge Lacasse',
          link: 'https://www.mus.ulaval.ca/notice.php?id=29',
          bio: 'Professor in Musicology at Université Laval.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/marc-leman.jpg',
          name: 'Marc Leman',
          link: 'https://research.flw.ugent.be/en/marc.leman',
          bio: 'Professor in systematic musicology and director of IPEM at Ghent University.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/xavier-serra.jpg',
          name: 'Xavier Serra',
          link: 'https://www.upf.edu/web/xavier-serra',
          bio: 'Professor of the Department of Information and Communication Technologies at Universitat Pompeu Fabra, Barcelona.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/jonathan-sterne.jpg',
          name: 'Jonathan Sterne',
          link: 'https://www.mcgill.ca/ahcs/people-contacts/faculty/sterne',
          bio: 'Professor and James McGill Chair in Culture and Technology at the Department of Art History and Communication Studies, McGill University.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/bilder/andy-tyrell.jpg',
          name: 'Andy Tyrell',
          link: 'https://www.york.ac.uk/electronic-engineering/staff/andy_tyrrell/',
          bio: 'Professor and Head of Department at the Department of Electronic Engineering, University of York.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/organisation/sab/bilder/peter_vuust.jpg',
          name: 'Peter Vuust',
          link: 'http://pure.au.dk/portal/en/persons/peter-vuust(2c697ab6-9b06-4a16-a687-c8cdbd56f661).html',
          bio: 'Professor at the Center for Music in the Brain, Aarhus University.'
        }
      ],
      people2: [
        {
          image: '/images/infographics/RITMO-Silhuett.svg',
          name: 'Peter Edwards',
          link: 'https://www.hf.uio.no/imv/english/people/aca/tenured/peterje/index.html',
          bio: 'Head of Department, Department of Musicology, University of Oslo'
        },
        {
          image: '/images/infographics/RITMO-Silhuett.svg',
          name: 'Ellen Munthe-Kaas',
          link: 'https://www.mn.uio.no/ifi/english/people/aca/ellenmk/index.html',
          bio: 'Head of Department, Department of Informatics, University of Oslo'
        },
        {
          image: '/images/infographics/RITMO-Silhuett.svg',
          name: 'Pål Kraft',
          link: 'https://www.sv.uio.no/psi/english/people/aca/paalkra/index.html',
          bio: 'Head of Department, Department of Psychology'
        }
      ],
      blocks1: [
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/innovasjonsprisen2018.jpg',
          heading: 'Innovation Prize',
          link: 'https://www.uio.no/om/aktuelt/pressemeldinger/2018/priser-til-uio-ansatte.html',
          text: 'The University of Oslo\'s Innovation prize for 2018 was awarded to RITMO\'s Centre Directors Anne Danielsen and Alexander Refsum Jensenius.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/laeng-dnva2018.jpeg',
          heading: 'Academy Membership',
          link: 'http://english.dnva.no/c40133/artikkel/vis.html?tid=40201',
          text: 'Bruno Laeng was elected member of in the Humanities and Social Sciences Division of the Norwegian Academy of Science and Letters in 2018.'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/20180508_174334.jpg',
          heading: 'EUA Committee',
          link: 'https://eua.eu/about/working-groups.html',
          text: 'Alexander Refsum Jensenius was appointed as the Norwegian representative to the EUA Expert Group on Science 2.0 / Open Science.'
        }
      ],
      blocks2: [
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/david.huron.jpg',
          heading: 'A Theory of Sadness: Melancholy, Grief, and Nostalgia',
          link: 'https://www.hf.uio.no/ritmo/english/news-and-events/events/seminars/2018/december/on-the-musically-sublime.html',
          text: 'David Huron, Ohio State University'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/andreaschiavio.jpg',
          heading: 'Being, Knowing, and Doing. 4E Cognition and the Dynamics of Musical Development',
          link: 'https://www.hf.uio.no/ritmo/english/news-and-events/events/seminars/2018/october/index.html',
          text: 'Andrea Schiavio, University of Graz'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/specht.jpg',
          heading: 'Rhythm, Tempo, and the Brain: fMRI studies in Bergen',
          link: 'https://www.hf.uio.no/ritmo/english/news-and-events/events/seminars/2018/september/index.html',
          text: 'Karsten Specht, University of Bergen'
        },
        {
          image: 'https://www.hf.uio.no/ritmo/english/about/yearly-report/images/maria-witek-200x300.jpg',
          heading: 'Musical Groove: Effect on pleasure, body-movement and the brain',
          link: 'https://www.hf.uio.no/ritmo/english/news-and-events/events/seminars/2018/june/index.html',
          text: 'Maria Witek, University of Birmingham'
        }
      ]
    }
  }
}
</script>

