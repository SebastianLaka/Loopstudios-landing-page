<script setup>
import FooterLogo from './FooterLogo.vue'
import FooterRights from './FooterRights.vue'
import FooterBar from './FooterBar.vue'
import FooterSocialMedia from './FooterSocialMedia.vue'

import IconFacebook from '../icons/icon-facebook.svg'
import IconTwitter from '../icons/icon-twitter.svg'
import IconPrinterest from '../icons/icon-pinterest.svg'
import IconInstagram from '../icons/icon-instagram.svg'
const footerLinks = [
  { id: 1, name: 'About' },
  { id: 2, name: 'Carrers' },
  { id: 3, name: 'Events' },
  { id: 4, name: 'Products' },
  { id: 5, name: 'Support' },
]
const footerSmIcons = [
  {
    id: 1,
    image: IconFacebook,
    alt: 'Facebook logo',
  },
  {
    id: 2,
    image: IconTwitter,
    alt: 'Twitter logo',
  },
  {
    id: 3,
    image: IconPrinterest,
    alt: 'Printerest logo',
  },
  {
    id: 4,
    image: IconInstagram,
    alt: 'Instagram logo',
  },
]
</script>
<template>
  <footer class="footer-container">
    <div class="footer-content wrapper">
      <FooterLogo />
      <div class="footer-bars">
        <FooterBar
          v-for="footerLink in footerLinks"
          :key="footerLink.id"
          :title="footerLink.name"
        />
      </div>
      <div class="footer-sm-icons">
        <FooterSocialMedia
          v-for="smIcon in footerSmIcons"
          :key="smIcon.id"
          :src="smIcon.image"
          :alt="smIcon.alt"
        />
      </div>
      <FooterRights> © 2021 Loopstudios. All rights reserved. </FooterRights>
    </div>
  </footer>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@media (min-width: 320px) {
  .footer-container {
    background-color: $main-black;
    padding: 3em 0;
    .footer-content {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 2em 0;
      .footer-bars {
        display: flex;
        flex-direction: column;
        align-items: center;
        list-style: none;
        gap: 1.5em 0;
      }
      .footer-sm-icons{
        display: flex;
        gap: 0 1em;
      }
    }
  }
}
</style>
