<template>
  <div class="gallery">
    <div v-for="image in images" :key="image.id" class="gallery-item" @click="openModal(image.src)">
      <img :src="image.src" :alt="image.alt" />
      <div class="card-overlay">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">Component</p>
          </header>
          <div class="card-content">
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec
              iaculis mauris.
              <a href="#">@bulmaio</a>. <a href="#">#css</a> <a href="#">#responsive</a>
              <br />
              <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">Save</a>
            <a href="#" class="card-footer-item">Share</a>
          </footer>
        </div>
      </div>
    </div>
    
    <div class="modal" :class="{ 'is-active': isModalActive, 'fade-in': isModalActive, 'fade-out': !isModalActive }">
      <div class="modal-background" @click="closeModal"></div>
      <div class="modal-content">
        <p class="image is-4by3">
          <img :src="modalImageSrc" alt="Modal Image">
        </p>
      </div>
      <button class="modal-close is-large" aria-label="close" @click="closeModal"></button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GalleryComponent',
  props: {
    images: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      isModalActive: false,
      modalImageSrc: ''
    };
  },
  methods: {
    openModal(imageSrc) {
      this.modalImageSrc = imageSrc;
      this.isModalActive = true;
    },
    closeModal() {
      this.isModalActive = false;
      this.modalImageSrc = '';
    }
  }
};
</script>

<style scoped>
.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.gallery-item {
  position: relative;
  box-sizing: border-box;
  flex: 1 1 calc(33.333% - 10px); /* Default to 3 per row */
}

.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
  cursor: pointer;
}

.card-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: none;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.5);
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}

.gallery-item:hover .card-overlay {
  display: flex;
  opacity: 1;
}

.card {
  width: 100%;
  max-width: 300px;
}

.modal.fade-in {
  animation: fadeIn 0.5s forwards;
}

.modal.fade-out {
  animation: fadeOut 0.5s forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

@media (max-width: 768px) {
  .gallery-item {
    flex: 1 1 calc(50% - 10px); /* 2 per row on mobile */
  }
  
  .gallery-item:hover .card-overlay {
    display: none;
  }
}
</style>