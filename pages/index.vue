<script setup>

</script>

<template>
    <div class="max-h-screen bg-[#DFF8FD]">
        <div class="static h-screen">
            <Navbar />
            <div class="flex flex-col md:flex-row justify-between items-center space-y-20 w-full">
                <div class="absolute top-1/3">
                    <div v-motion :initial="{ x: -200, opacity: 0, }"
                        :enter="{ x: 0, opacity: 1, transition: { duration: 1500, type: 'keyframes', ease: 'easeOut' } }"
                        class="mx-4 text-4xl md:text-7xl text-black">Web <span>Developer</span>
                    </div>
                    <div v-motion :initial="{ y: 200, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 2100, type: 'keyframes', ease: 'easeOut' } }"
                        class="mx-4  text-gray-400 text-xl md:text-3xl">Olaaa, my name is wildy</div>
                    <div v-motion :initial="{ y: 400, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 2700, type: 'keyframes', ease: 'easeOut' } }">
                        <a href="/docs/wildy.pdf" class="mx-4 text-gray-400 text-xl" download>Download My CV</a>
                    </div>
                </div>
                <img v-motion :initial="{ y: 500, opacity: 0, }"
                    :enter="{ y: 0, opacity: 1, transition: { duration: 3000, type: 'keyframes', ease: 'easeOut' } }"
                    src="/avatar.png" alt="avatar" class="absolute bottom-0 right-0 z-50 w-auto h-60 md:h-auto">
            </div>
        </div>
    </div>
</template>
