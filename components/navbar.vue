<template>
    <div class="bg-[#DFF8FD] w-full p-2 flex space-x-4 justify-end">
        <nuxtLink v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 1200,  type: 'keyframes', ease: 'easeOut'}}" to="/" class="text-black">Home</nuxtLink>
        <nuxtLink v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 900,  type: 'keyframes', ease: 'easeOut'}}" to="/about"  class="text-black">About Me</nuxtLink>
        <nuxtLink v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 600,  type: 'keyframes', ease: 'easeOut'}}" to="/contact"  class="text-black">Contact</nuxtLink>
        <div v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 300,  type: 'keyframes', ease: 'easeOut'}}"  class="text-black">Portofolio</div>
    </div>
</template>

<style scoped>
a.router-link-active,
a.router-link-exact-active {
  @apply rounded-lg text-emerald-500;
}
a.router-link-active > div,
a.router-link-exact-active > div {
  @apply text-primary-900;
}
</style>