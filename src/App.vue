<script setup>
import BgMusic from './components/BgMusic.vue'
import LandingOverlay from './components/LandingOverlay.vue'
import TopBar from './components/TopBar.vue'
import Invitation from './components/Invitation.vue'
import Profile from './components/Profile.vue'
import FallingFlowers from './components/FallingFlowers.vue'
import Gallery from './components/Gallery.vue'
import Location from './components/Location.vue'
import Calendar from './components/Calendar.vue'
import Countdown from './components/Countdown.vue'
import Information from './components/Information.vue'
import Account from './components/Account.vue'
import Footer from './components/Footer.vue'

const images = [
  `${import.meta.env.BASE_URL}images/2.jpg`,
  `${import.meta.env.BASE_URL}images/3.jpg`,
  `${import.meta.env.BASE_URL}images/4.jpg`,
  `${import.meta.env.BASE_URL}images/5.jpg`,
  `${import.meta.env.BASE_URL}images/6.jpg`,
  `${import.meta.env.BASE_URL}images/7.jpg`,
  `${import.meta.env.BASE_URL}images/8.jpg`,
  `${import.meta.env.BASE_URL}images/9.jpg`,
  `${import.meta.env.BASE_URL}images/10.jpg`,
  `${import.meta.env.BASE_URL}images/11.jpg`,
  `${import.meta.env.BASE_URL}images/12.jpg`,
  `${import.meta.env.BASE_URL}images/13.jpg`,
]
const weddingDate = new Date('2025-09-21T12:00:00')
</script>

<template>
  <!--
  <LandingOverlay />
  -->
  <FallingFlowers />
  <div class="container">
    <BgMusic />
    <TopBar />
    <Invitation />
    <Profile />
    <Gallery :images="images" />
    <Location />
    <Calendar :year="2025" :month="8" :pinned-day="21" />
    <Countdown :targetDate="weddingDate" />
    <Information />
    <Account />
    <Footer />
  </div>
</template>

<style scoped>
.container {
  max-width: 480px;         /* typical mobile max */
  margin: 0 auto;
  width: 100%;
  background: white;        /* optional background */
}
</style>
