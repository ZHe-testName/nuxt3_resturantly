<template>
  <slot name="header" />

  <img 
    src="https://www.iconpacks.net/icons/2/free-sad-face-icon-2691-thumb.png"
    alt="sad_face"
  />

  <slot name="redirectEl" />
</template>

<style scoped>
  img {
    width: 10rem;
  }
</style>