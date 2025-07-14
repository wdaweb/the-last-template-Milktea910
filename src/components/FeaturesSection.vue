<template>
  <section class="full-vh-section parallax-bg">
    <div class="circle-container">
      <div class="main-circle">
        <div class="outer-circle"></div>
        <div class="circle-text">{{ circleTexts[selectedIndex] }}</div>
        <button
          v-for="(text, i) in circleTexts"
          :key="i"
          class="small-circle circle-btn"
          @click="selectedIndex = i"
        >
          <q-icon size="large" :name="iconClasses[i]" class="icon-center"></q-icon>
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.full-vh-section {
  height: 80vh;
  position: relative;
  overflow: hidden;
}

.circle-container {
  position: absolute;
  left: 15%;
  top: 50%;
  transform: translateY(-50%) scale(1); /* 初始 scale 設為 1 */
  width: 500px;
  height: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition:
    transform 0.3s,
    left 0.3s;
}
.main-circle {
  position: relative;
  width: 200px;
  height: 200px;
  background: #000;
  border-radius: 50%;
  z-index: 5;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
.circle-text {
  font-family: Arial, 'sans-serif';
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
  font-size: 25px;
  font-weight: normal;
  text-align: center;
  pointer-events: none;
  z-index: 4;
  letter-spacing: 3px;
}
.outer-circle {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  height: 300px;
  border: 2px solid #000;
  border-radius: 50%;
  z-index: 1;
}

button.circle-btn.small-circle {
  position: absolute;
  width: 50px;
  height: 50px;
  background: #000;
  border-radius: 50%;
  box-shadow: 0 0 4px #0002;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border: none;
  cursor: pointer;
  transition:
    background 0.2s,
    box-shadow 0.2s;
  pointer-events: auto;
  will-change: transform;
  z-index: 3;
  display: flex;
  align-items: center;
  justify-content: center;
}
.icon-center {
  color: #fff;
  font-size: 1.5rem;
  pointer-events: none;
}
button.circle-btn.small-circle:hover {
  background: #222;
  box-shadow: 0 0 12px #0006;
}

.parallax-bg {
  background-image: url('https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/05/laptop.jpeg');
  background-attachment: fixed;
  background-position: center top;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>

<script setup>
import { ref, onMounted } from 'vue'
import gsap from 'gsap'

const circleTexts = [
  'Done Awesomely',
  '100% Mobile Ready',
  'Award Winning',
  'New Technology',
  'Ultimate Solution',
  'Brand New Features',
]
const iconClasses = [
  'fa-solid fa-headphones',
  'fa-solid fa-gears',
  'fa-solid fa-users',
  'fa-solid fa-flask',
  'fa-solid fa-umbrella',
  'fa-solid fa-house',
]
const selectedIndex = ref(0)

onMounted(() => {
  const section = document.querySelector('.circle-container')
  const circles = document.querySelectorAll('.small-circle')
  function animateCircles() {
    const rect = section.getBoundingClientRect()
    if (rect.top < window.innerHeight && rect.bottom > 0) {
      circles.forEach((circle, i) => {
        const angle = (i * Math.PI * 2) / 6
        const radius = 150
        const x = radius * Math.cos(angle)
        const y = radius * Math.sin(angle)
        gsap.to(circle, {
          x: x,
          y: y,
          duration: 1.2,
          delay: i * 0.1,
          ease: 'power2.out',
        })
      })
      window.removeEventListener('scroll', animateCircles)
    }
  }
  // 動態調整 scale 與 left
  function updateScale() {
    const vw = window.innerWidth
    let scale = 1
    let left = '15%'
    if (vw < 600) {
      scale = 0.8
      left = '5%'
    } else if (vw < 900) {
      scale = 1
      left = '10%'
    } else {
      scale = 1.5
      left = '15%'
    }
    section.style.transform = `translateY(-50%) scale(${scale})`
    section.style.left = left
  }
  window.addEventListener('resize', updateScale)
  updateScale()
  // 初始位置在中心
  circles.forEach((circle) => {
    gsap.set(circle, { x: 0, y: 0 })
  })
  window.addEventListener('scroll', animateCircles)
  // 若一開始就可見，直接觸發
  animateCircles()
})
</script>
