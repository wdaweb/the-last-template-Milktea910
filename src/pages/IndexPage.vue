<template>
  <q-page class="q-pa-none">
    <HeroSection id="Hero" />

    <AboutSection id="About" />

    <ChooseSection id="Choose" />

    <FeaturesSection id="Feature" />

    <PresaleSection id="Sale" />

    <PortfolioSection id="Work" />

    <ClientSection id="Client" />

    <ContactsSection id="Contacts" />

    <MapSection id="Map" />

    <FooterSection id="Footer" />
  </q-page>
</template>

<script setup>
import HeroSection from 'components/HeroSection.vue'
import ChooseSection from 'src/components/ChooseSection.vue'
import FeaturesSection from 'components/FeaturesSection.vue'
import AboutSection from 'components/AboutSection.vue'
import PresaleSection from 'src/components/PresaleSection.vue'
import PortfolioSection from 'src/components/PortfolioSection.vue'
import ClientSection from 'src/components/ClientSection.vue'
import ContactsSection from 'src/components/ContactsSection.vue'
import MapSection from 'src/components/MapSection.vue'
import FooterSection from 'src/components/FooterSection.vue'
</script>
