<template>
  <section class="full-vh-section">
    <div class="container">
      <div class="row">
        <div class="col-12 text-center">
          <div class="about_title">WE ARE HAZEL</div>
          <div class="about_subtitle">ABOUT US</div>
          <div class="content">
            <p>
              Assertively impact bricks-and-clicks outsourcing after mission-critical ROI.
              Monotonectally <br />
              underwhelm cost effective convergence without granular alignments. Progressively
              create <br />
              client-based platforms.
            </p>
          </div>
        </div>
      </div>
      <div class="image-wrapper">
        <img
          src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/work-team1.jpg"
          class="bottom-image"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.full-vh-section {
  height: 75vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}
.about_title {
  font-family: 'Hind', 'Arial', 'sans-serif' !important;
  font-weight: 600;
  font-size: 12px;
  color: #303030;
  line-height: 1.3em;
  letter-spacing: 3px;
  text-transform: uppercase;
}
.about_subtitle {
  font-size: 50px;
  text-align: center;
  font-family: 'Hind', 'Arial', 'sans-serif';
  font-weight: 300;
  color: #303030;
  line-height: 1.3em;
  letter-spacing: 10px;
  text-transform: uppercase;
}
.content {
  font-family: 'Mulish', 'Arial', 'sans-serif';
  font-weight: normal;
  font-size: 14px;
  color: #595959;
  text-align: center;
  line-height: 1.7em !important;
  margin-bottom: 1em !important;
}

.image-wrapper {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
}

.bottom-image {
  height: auto;
  width: auto; /* 固定寬度，可依需求調整 */
  vertical-align: top;
  filter: grayscale(100%);
  transition: filter 0.5s ease;
}

.bottom-image:hover {
  filter: grayscale(0%);
}
</style>
