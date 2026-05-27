<template>
  <div class="club-photo-wrap" :style="{ height: height }">
    <img src="../images/photo_asand.png" :alt="alt" class="club-photo" />
  </div>
</template>

<script setup>
defineProps({
  height: {
    type: String,
    default: '300px'
  },
  alt: {
    type: String,
    default: 'Photo du club ASANDTT Marseille'
  }
})
</script>

<style scoped>
.club-photo-wrap {
  width: 100%;
  overflow: hidden;
  border-radius: 12px;
}
.club-photo {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>