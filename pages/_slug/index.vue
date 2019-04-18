<template>
  <div>
    <div class="image-header">
      This page is in progress
    </div>
    <div class="image-list">
      <img src="~/assets/img/five-1.jpg" alt="" />
      <img src="~/assets/img/five-2.jpg" alt="" />
      <img src="~/assets/img/five-3.jpg" alt="" />
      <img src="~/assets/img/five.jpg" alt="" />
    </div>
  </div>
</template>

<style scoped>
.image-header {
  background: lightgray;
  margin-bottom: 2rem;
  padding: 2rem;
}
.image-list {
  display: flex;
  flex-direction: column;
}
.image-list img {
  width: 90%;
  max-height: 600px;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.27), 0 0 40px rgba(0, 0, 0, 0.06) inset;
  margin-bottom: 1rem;
}
</style>
