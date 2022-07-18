<template>
  <section class="cropper">
    <VueCropper
      ref="cropper" 
      auto-crop
      mode="cover"
      img="https://avatars.githubusercontent.com/u/15681693?s=88&u=2097736bf929136febb8c52df09f10290930fdef&v=1"
    >
    </VueCropper>
    <button @click="getData">获取截图</button>
  </section>
</template>

<script setup>
import 'vue-cropper/dist/index.css'
import { VueCropper }  from "vue-cropper";
import { ref } from '@vue/runtime-core';

const cropper = ref(null)

const getData = () => {
  cropper.value.getCropData(data => {
    const img = document.createElement('img')
    img.src = data;
    document.body.append(img)
  })
}

</script>

<style>
.cropper {
  width: 500px;
  height: 500px;
}
</style>
