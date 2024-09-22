<template>
  <div class="container">
    <section class="hero box m-6" :style="heroStyle">
      <div class="hero-body">
        <p class="title">The Chapels</p>
        <p class="subtitle">Featuring The Chapels of Each Barangay</p>
      </div>
    </section>
    <div class="tabs is-centered is-boxed">
      <ul>
        <li :class="{ 'is-active': activeTab === 'Paralaya', 'tab-animation': activeTab === 'Paralaya' }" @click="switchTab('Paralaya')"><a>Paralaya</a></li>
        <li :class="{ 'is-active': activeTab === 'Buas', 'tab-animation': activeTab === 'Buas' }" @click="switchTab('Buas')"><a>Buas</a></li>
        <li :class="{ 'is-active': activeTab === 'Pescadores', 'tab-animation': activeTab === 'Pescadores' }" @click="switchTab('Pescadores')"><a>Pescadores</a></li>
        <li :class="{ 'is-active': activeTab === 'Bambang', 'tab-animation': activeTab === 'Bambang' }" @click="switchTab('Bambang')"><a>Bambang</a></li>
        <li :class="{ 'is-active': activeTab === 'Gulap', 'tab-animation': activeTab === 'Gulap' }" @click="switchTab('Gulap')"><a>Gulap</a></li>
        <li :class="{ 'is-active': activeTab === 'Sto. Rosario', 'tab-animation': activeTab === 'Sto. Rosario' }" @click="switchTab('Sto. Rosario')"><a>Sto. Rosario</a></li>
        <li :class="{ 'is-active': activeTab === 'San Agustin', 'tab-animation': activeTab === 'San Agustin' }" @click="switchTab('San Agustin')"><a>San Agustin</a></li>
      </ul>
    </div>
    <GalleryComponent :images="images[activeTab]" />
  </div>
</template>

<script>
import GalleryComponent from '@/components/GalleryComponent.vue';

export default {
  components: {
    GalleryComponent,
 
  },
  data() {
    return {
      activeTab: 'Paralaya',
      images: {
        Paralaya: [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 1' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 2' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 3' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 4' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 5' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 6' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 7' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 8' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 9' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 10' }
        ],
        Buas: [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 11' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 12' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 13' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 14' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 15' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 16' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 17' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 18' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 19' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 20' }
        ],
        Pescadores: [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 21' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 22' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 23' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 24' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 25' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 26' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 27' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 28' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 29' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 30' }
        ],
        Bambang: [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 31' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 32' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 33' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 34' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 35' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 36' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 37' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 38' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 39' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 40' }
        ],
        Gulap: [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 41' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 42' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 43' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 44' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 45' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 46' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 47' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 48' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 49' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 50' }
        ],
        'Sto. Rosario': [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 51' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 52' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 53' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 54' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 55' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 56' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 57' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 58' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 59' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 60' }
        ],
        'San Agustin': [
          { id: 1, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 61' },
          { id: 2, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 62' },
          { id: 3, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 63' },
          { id: 4, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 64' },
          { id: 5, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 65' },
          { id: 6, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 66' },
          { id: 7, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 67' },
          { id: 8, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 68' },
          { id: 9, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 69' },
          { id: 10, src: 'https://bulma.io/assets/images/placeholders/1280x960.png', alt: 'Image 70' }
        ]
      },
      heroStyle: {
        backgroundImage: 'url(@/assets/images/SAAP.jpg) !important',
        backgroundSize: 'cover !important',
        backgroundPosition: 'center !important'
      }
    };
  },
  methods: {
    switchTab(tab) {
      this.activeTab = tab;
    }
  }
};
</script>

<style scoped>
.tab-animation {
  transition: all 0.3s ease;
}
</style>