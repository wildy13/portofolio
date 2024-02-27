<script setup>

</script>

<template>
    <div class="max-h-screen bg-[#DFF8FD]">
        <div class="h-screen flex flex-col justify-center">
            <div class="flex justify-between items-center space-y-20">
                <div class="mb-72 md:m-0">
                    <div v-motion :initial="{ x: -200, opacity: 0, }"
                        :enter="{ x: 0, opacity: 1, transition: { duration: 1500, type: 'keyframes', ease: 'easeOut' } }"
                        class="pt-10 mx-4 text-4xl text-black">Web <span>Developer</span>
                    </div>
                    <div v-motion :initial="{ y: 200, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 2100, type: 'keyframes', ease: 'easeOut' } }"
                        class="mx-4  text-gray-400 text-xl">Olaaa, my name is wildy</div>
                    <div v-motion :initial="{ y: 200, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 2400, type: 'keyframes', ease: 'easeOut' } }"
                        class="mx-4 text-gray-400 text-xl">The biggest thing i know is <span
                            class="text-red-500">Never</span> Give up</div>
                </div>
                <img v-motion :initial="{ y: 375, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 2700, type: 'keyframes', ease: 'easeOut' } }" src="/avatar.png" alt="avatar" class="absolute bottom-0 right-0 z-50 h-auto">
            </div>
        </div>
    </div>
</template>