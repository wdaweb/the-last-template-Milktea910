<template>
  <section class="full-vh-section">
    <div class="container full-height">
      <div class="row full-height">
        <div class="col-12 flex justify-center items-center">
          <div class="choose_title text-center">WHY CHOOSE US?</div>
          <swiper
            :loop="true"
            :slidesPerView="slidesPerView"
            :spaceBetween="30"
            :pagination="{
              clickable: true,
            }"
            :modules="[Navigation]"
            :navigation="true"
            class="mySwiper"
          >
            <swiper-slide>
              <div class="flex wrap justify-center items-center text-center">
                <div class="icon" style="height: 60px">
                  <q-icon class="text-center text-white" size="lg" name="fa-solid fa-palette" />
                </div>
                <div>
                  <div class="contentHeader text-center">UNLIMITED COLORS</div>
                  <div class="contentDescription text-center">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing integer sodales vel eros
                      quis consequat.
                    </p>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex wrap justify-center items-center text-center">
                <div class="icon" style="height: 60px">
                  <q-icon
                    class="text-center text-white"
                    size="lg"
                    name="fa-solid fa-ranking-star"
                  />
                </div>
                <div>
                  <div class="contentHeader text-center">UNLIMITED COLORS</div>
                  <div class="contentDescription text-center">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing integer sodales vel eros
                      quis consequat.
                    </p>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex wrap justify-center items-center text-center">
                <div class="icon" style="height: 60px">
                  <q-icon class="text-center text-white" size="lg" name="fa-solid fa-inbox" />
                </div>
                <div>
                  <div class="contentHeader text-center">UNLIMITED COLORS</div>
                  <div class="contentDescription text-center">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing integer sodales vel eros
                      quis consequat.
                    </p>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex wrap justify-center items-center text-center">
                <div class="icon" style="height: 60px">
                  <q-icon
                    class="text-center text-white"
                    size="lg"
                    name="fa-solid fa-feather-pointed"
                  />
                </div>
                <div>
                  <div class="contentHeader text-center">UNLIMITED COLORS</div>
                  <div class="contentDescription text-center">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing integer sodales vel eros
                      quis consequat.
                    </p>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex wrap justify-center items-center text-center">
                <div class="icon" style="height: 60px">
                  <q-icon class="text-center text-white" size="lg" name="fa-solid fa-tv" />
                </div>
                <div>
                  <div class="contentHeader text-center">UNLIMITED COLORS</div>
                  <div class="contentDescription text-center">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing integer sodales vel eros
                      quis consequat.
                    </p>
                  </div>
                </div>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex wrap justify-center items-center text-center">
                <div class="icon" style="height: 60px">
                  <q-icon class="text-center text-white" size="lg" name="fa-solid fa-globe" />
                </div>
                <div>
                  <div class="contentHeader text-center">UNLIMITED COLORS</div>
                  <div class="contentDescription text-center">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing integer sodales vel eros
                      quis consequat.
                    </p>
                  </div>
                </div>
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.full-vh-section {
  background: #000;
  height: 60vh;
}
.choose_title {
  font-size: 35px;
  color: #ffffff;
  text-align: center;
  font-family: 'Hind', 'Arial', 'sans-serif';
  font-weight: 300;
  letter-spacing: 3px;
  text-transform: uppercase;
}
.contentHeader {
  font-family: 'Open Sans';
  font-weight: 600;
  color: #b8b8b8;
  font-size: 14px;
}
.contentDescription {
  padding: 0 50px;
  color: #999999;
  font-family: 'Mulish', 'Arial', 'sans-serif';
  font-weight: normal;
  font-size: 14px;
}
.swiper {
  width: 100%;
  height: 50%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: transparent;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  /* display: block; */
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/navigation'
import { Navigation } from 'swiper/modules'

const slidesPerView = ref(3)

function updateSlidesPerView() {
  const width = window.innerWidth
  if (width < 768) {
    slidesPerView.value = 1
  } else if (width < 1024) {
    slidesPerView.value = 2
  } else {
    slidesPerView.value = 3
  }
}

onMounted(() => {
  updateSlidesPerView()
  window.addEventListener('resize', updateSlidesPerView)
})

onBeforeUnmount(() => {
  window.removeEventListener('resize', updateSlidesPerView)
})
</script>
