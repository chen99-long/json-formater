<script lang="ts" setup>
import Browser from 'webextension-polyfill'
import logo from '../assets/icon-512.png'

const openHomePage = () => {
  window.open(Browser.runtime.getManifest().homepage_url, '_blank')
}
</script>

<template>
  <a class="icon-btn mx-2 text-2xl" rel="noreferrer" target="_blank" title="GitHub" @click="openHomePage">
    <img class="b-rd-50% w2em" :src="logo" alt="">
  </a>
</template>
