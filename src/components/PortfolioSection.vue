<template>
  <section class="full-vh-section">
    <div class="text-center">
      <div class="about_title">WE BUILD GOOD STUFF</div>
      <div class="about_subtitle">OUR PORTFOLIO</div>
      <div class="content">
        <p>
          Assertively impact bricks-and-clicks outsourcing after mission-critical ROI.
          Monotonectally <br />
          underwhelm cost effective convergence without granular alignments. Progressively create
          <br />
          client-based platforms.
        </p>
      </div>
    </div>
    <div class="container">
      <div class="row portfolio-row justify-center">
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(0)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax1.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(1)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax23.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(2)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax33.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(3)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax43.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(4)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax7-1.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(5)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax52.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(6)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax777.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(7)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax8.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(8)">
            <img
              src="https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax9.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(9)">
            <img
              src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/SingleProjectAjax103.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(10)">
            <img
              src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/SingleProjectAjax112.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-sm-6 col-lg-4 flex justify-center">
          <div class="portfolio-card" @click="openLightbox(11)">
            <img
              src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/SingleProjectAjax12.jpg"
              alt="Portfolio"
              class="portfolio-img"
            />
            <div class="portfolio-bar">
              <div class="portfolio-title">Card Title</div>
              <div class="portfolio-content">
                This is the card content. You can describe your project here.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <vue-easy-lightbox
    :visible="visibleRef"
    :imgs="imgsRef"
    :index="indexRef"
    @hide="onHide"
  ></vue-easy-lightbox>
</template>

<script setup>
import { ref } from 'vue'
import VueEasyLightbox from 'vue-easy-lightbox'

const images = [
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax1.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax23.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax33.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax43.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax7-1.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax52.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax777.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax8.jpg',
  'https://preview.treethemes.com/hazel/demo1clean/wp-content/uploads/sites/2/2021/04/SingleProjectAjax9.jpg',
  'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/SingleProjectAjax103.jpg',
  'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/SingleProjectAjax112.jpg',
  'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/SingleProjectAjax12.jpg',
]

const visibleRef = ref(false)
const indexRef = ref(0)
const imgsRef = ref(images)

function openLightbox(idx) {
  indexRef.value = idx
  visibleRef.value = true
}
function onHide() {
  visibleRef.value = false
}
</script>

<style scoped>
.full-vh-section {
  height: 180vh;
  position: relative;
}
@media (max-width: 1024px) {
  .full-vh-section {
    height: 450vh;
  }
}
@media (min-width: 1025px) and (max-width: 1440px) {
  .full-vh-section {
    height: 250vh;
  }
}

/* 卡片結構 */
.portfolio-card {
  position: relative;
  width: 100%;
  max-width: 400px;
  height: 300px;
  margin-bottom: 0;
  overflow: hidden;
  border-radius: 0;
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.12);
  display: flex;
  flex-direction: column;
}
.portfolio-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  filter: grayscale(100%);
  transition:
    filter 0.4s cubic-bezier(0.4, 0, 0.2, 1),
    transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}
.portfolio-card:hover .portfolio-img {
  filter: grayscale(0%);
  transform: translateY(-60px);
}
.portfolio-bar {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 60px;
  background: #222;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transform: translateY(100%);
  transition:
    opacity 0.4s cubic-bezier(0.4, 0, 0.2, 1),
    transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  z-index: 2;
  padding: 0 16px;
  box-sizing: border-box;
}
.portfolio-card:hover .portfolio-bar {
  opacity: 1;
  transform: translateY(0);
}
.portfolio-title {
  color: #fff;
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 2px;
  text-align: center;
  letter-spacing: 2px;
}
.portfolio-content {
  color: #fff;
  font-size: 13px;
  text-align: center;
  line-height: 1.2;
}
.about_title {
  font-family: 'Hind', 'Arial', 'sans-serif' !important;
  font-weight: 600;
  font-size: 12px;
  color: #303030;
  line-height: 1.3em;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-top: 10rem;
}
.about_subtitle {
  font-family: 'Hind', 'Arial', 'sans-serif';
  font-weight: 300;
  font-size: 40px;
  color: #303030;
  line-height: 1.3em;
  letter-spacing: 10px;
  text-transform: uppercase;
  text-align: center;
  margin-top: 10px;
  margin-bottom: 20px;
}
.content {
  font-family: 'Mulish', 'Arial', 'sans-serif';
  font-weight: normal;
  font-size: 14px;
  color: #595959;
  text-align: center;
  line-height: 1.7em !important;
  margin-bottom: 5em !important;
}
.about_subtitle {
  font-family: 'Hind', 'Arial', 'sans-serif';
  font-weight: 300;
  font-size: 40px;
  color: #303030;
  line-height: 1.3em;
  letter-spacing: 10px;
  text-transform: uppercase;
  text-align: center;
  margin-top: 10px;
  margin-bottom: 20px;
}
.content {
  font-family: 'Mulish', 'Arial', 'sans-serif';
  font-weight: normal;
  font-size: 14px;
  color: #595959;
  text-align: center;
  line-height: 1.7em !important;
  margin-bottom: 5em !important;
}
</style>
