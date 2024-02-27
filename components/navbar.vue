<template>
    <div class="fixed top-0 left-0 z-50 bg-[#DFF8FD] w-full p-2 flex space-x-4 justify-end">
        <nuxtLink v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 1200,  type: 'keyframes', ease: 'easeOut'}}" to="/" class="text-black">Home</nuxtLink>
        <nuxtLink v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 900,  type: 'keyframes', ease: 'easeOut'}}" to="/about"  class="text-black">About Me</nuxtLink>
        <div v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 600,  type: 'keyframes', ease: 'easeOut'}}"  class="text-black">Contact</div>
        <div v-motion :initial="{ x: -100, opacity: 0, }" :enter="{ x: 0, opacity: 1, transition: { duration: 300,  type: 'keyframes', ease: 'easeOut'}}"  class="text-black">Portofolio</div>
    </div>
</template>