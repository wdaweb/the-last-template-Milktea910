<template>
  <section class="full-client-section">
    <div class="container full-height">
      <div class="row justify-center items-center text-center">
        <div class="col-12 client-title">OUR CLIENTS FEEDBACK</div>
        <div class="col-12">
          <img
            v-for="(img, idx) in imgs"
            :key="img.src"
            :src="img.src"
            @mouseenter="activeIndex = idx"
            @mouseleave="activeIndex = null"
            class="client-img"
            :class="{ active: activeIndex === idx }"
          />
        </div>
        <div class="col-12 col-md-3 client-review">
          {{ activeIndex !== null ? imgs[activeIndex].text : '' }}
        </div>
      </div>
      <q-separator class="center" style="width: 50%" />
      <div class="client-bottom-imgs flex">
        <img
          src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/11-300x171-1.png"
        />

        <img
          src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/8-300x171-dark.png"
        />

        <img
          src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/7-300x171-dark.png"
        />

        <img
          src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/8-300x171-dark2.png"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: null,
      imgs: [
        {
          src: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/t1.jpeg',
          text: 'Dynamically whiteboard timely models through bricks-and-clicks e-services. Holisticly predominate resource maximizing users through backend leadership skills. Continually mesh team building strategic theme areas without standards compliant users. Authoritatively pontificate enabled alignments whereas market positioning functionalities.',
        },
        {
          src: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/t4.jpeg',
          text: 'Professionally administrate business web services without future-proof catalysts for change.',
        },
        {
          src: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/t5.jpeg',
          text: 'Credibly envisioneer enterprise-wide content before resource maximizing leadership skills. Progressively visualize professional value via distributed value. Efficiently restore adaptive bandwidth through best-of-breed outsourcing. Appropriately redefine professional sources with extensible strategic theme areas. Progressively exploit plug-and-play ROI and excellent platforms',
        },
        {
          src: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/t2.jpeg',
          text: 'Compellingly e-enable distributed deliverables whereas customer directed vortals. Objectively pontificate leveraged collaboration and idea-sharing without bleeding-edge resources. Professionally administrate business web services without future-proof catalysts for change. Energistically engage diverse vortals and prospective methods of empowerment. Competently pontificate diverse',
        },
        {
          src: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/t3.jpeg',
          text: 'Enthusiastically syndicate inexpensive services and 24/7 bandwidth. Phosfluorescently develop cooperative content vis-a-vis best-of-breed alignments. Competently innovate orthogonal e-tailers via interactive core competencies. Uniquely implement transparent',
        },
        {
          src: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/t6.jpeg',
          text: 'Rapidiously integrate multimedia based resources whereas low-risk high-yield technologies. Proactively innovate market positioning products without B2B products. Progressively recaptiualize',
        },
      ],
    }
  },
}
</script>

<style scoped>
.center {
  position: relative;
  left: 50%;
  top: 10%;
  transform: translate(-50%);
}
.full-client-section {
  min-height: 100vh;
  background: #f0efef;
  position: relative;
  display: flex;
  flex-direction: column;
}
.container.full-height {
  flex: 1 1 auto;
}
.client-bottom-imgs {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  gap: 24px;
  padding-bottom: 32px;
  z-index: 10;
  position: absolute;
  left: 0;
  bottom: 0;
}
.client-bottom-imgs img {
  width: 300px;
  object-fit: contain;
  margin: 0 8px;
  filter: drop-shadow(0 2px 8px rgba(0, 0, 0, 0.08));
}
.client-img {
  width: 50px;
  height: 50px;
  object-fit: cover;
  margin: 0 8px;
  cursor: pointer;
  border-radius: 50%;
  border: 2px solid #eee;
  opacity: 0.5;
  transition:
    opacity 0.3s,
    border-color 0.2s;
}
.client-img.active {
  opacity: 1;
}
.client-review {
  font-family: 'Mulish', 'Arial', 'sans-serif';
  width: 50%;
  margin-top: 32px;
  min-height: 40px;
  font-size: 16px;
  color: #5c5c5c;
  font-weight: normal;
  text-align: center !important;
  line-height: 1.7em !important;
}
.client-title {
  text-align: center;
  font-family: 'Hind', 'Arial', 'sans-serif';
  font-weight: 300;
  font-size: 32px;
  color: #303030;
  line-height: 1.3em;
  letter-spacing: 10px;
  text-transform: uppercase;
  margin-top: 10rem;
  margin-bottom: 20px;
}
@media (max-width: 768px) {
  .client-bottom-imgs {
    flex-wrap: wrap;
    gap: 12px;
    padding-bottom: 16px;
    position: static;
  }
}
</style>
