<template>
  <section class="full-vh-section">
    <div class="contact-overlay">
      <div class="contacts-title">We would love to know you</div>
      <div class="contacts-subtitle">GET IN TOUCH WITH US</div>
      <div class="container">
        <div class="row flex-center">
          <div class="col-12 col-md-4">
            <q-input
              square
              outlined
              v-model="text"
              color="white"
              label="Name"
              label-color="white"
            />
          </div>
          <div class="col-12 col-md-4">
            <q-input
              square
              outlined
              v-model="text"
              color="white"
              label="Email"
              label-color="white"
            />
          </div>
          <div class="col-12 col-md-4">
            <q-input
              square
              outlined
              v-model="text"
              color="white"
              label="Subject"
              label-color="white"
            />
          </div>
          <div class="col-12" style="margin-top: 1rem">
            <q-input
              v-model="text"
              square
              outlined
              type="textarea"
              label-color="white"
              color="white"
              label="Message"
            />
          </div>
          <q-btn class="sale_button" label="CONTACT US" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.sale_button {
  margin-top: 1rem;
  border-radius: 0;
  border: 3px solid transparent;
  padding: 7px 11px;
  border-color: rgb(255, 255, 255);
  color: rgb(255, 255, 255);
  background-color: transparent;
}
.contacts-title {
  letter-spacing: 10px;
  margin-top: 10rem;
  text-align: center;
  font-family: 'Open Sans';
  font-weight: 700;
  color: #adadad;
  font-size: 14px;
  line-height: 30px;
  margin-bottom: 1rem;
}
.contacts-subtitle {
  margin-top: 1rem;
  margin-bottom: 5rem;
  font-size: 38px;
  color: #f2f2f2;
  line-height: 42px;
  text-align: center;
  font-family: 'Hind', 'Arial', 'sans-serif';
  font-weight: 300;
  line-height: 1.3em;
  letter-spacing: 10px;
  text-transform: uppercase;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
}
.full-vh-section {
  height: 100vh;
  background: url('https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/05/contactform.jpeg')
    no-repeat center/cover;
  position: relative;
}
.contact-overlay {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  z-index: 1;
}
</style>

<script setup>
import { ref } from 'vue'
const text = ref('')
</script>
