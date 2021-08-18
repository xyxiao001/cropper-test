<template>
  <section class="cropper">
    <VueCropper img="https://avatars.githubusercontent.com/u/15681693?s=88&u=2097736bf929136febb8c52df09f10290930fdef&v=4"></VueCropper>
  </section>
</template>

<script setup>
import 'vue-cropper/dist/index.css'
import { VueCropper }  from "vue-cropper";

</script>

<style>
.cropper {
  width: 500px;
  height: 500px;
}
</style>
