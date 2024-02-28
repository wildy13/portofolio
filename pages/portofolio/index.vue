<script setup>
const items = [
    '/images/image-1.jpeg',
    '/images/image-2.jpeg',
    '/images/image-3.jpeg',
    '/images/image-4.jpeg',
    'https://picsum.photos/600/800?random=3',
    'https://picsum.photos/600/800?random=4',
    'https://picsum.photos/600/800?random=5',
    'https://picsum.photos/600/800?random=6'
]
</script>

<template>
    <div class="max-h-screen bg-[#DFF8FD]">
        <div class="h-screen">
            <Navbar />
            <div class="md:hidden">
                <div class="py-2 text-center font-semibold text-base">Highlight Project</div>
                <div class=" grid grid-cols-2 mx-2 gap-2">
                    <div class="grid gap-1">
                        <div v-motion :initial="{ scale: 0, opacity: 0, }"
                            :enter="{ scale: 1, opacity: 1, transition: { duration: 500, type: 'keyframes', ease: 'easeOut' } }">
                            <img class="h-auto max-w-full rounded-lg" src="/images/image-1.jpeg">
                        </div>
                        <div v-motion :initial="{ scale: 0, opacity: 0, }"
                            :enter="{ scale: 1, opacity: 1, transition: { delay: 500, duration: 500, type: 'keyframes', ease: 'easeOut' } }">
                            <img class="h-auto max-w-full rounded-lg" src="/images/image-2.jpeg">
                        </div>
                    </div>
                    <div class="grid gap-1">
                        <div v-motion :initial="{ scale: 0, opacity: 0, }"
                            :enter="{ scale: 1, opacity: 1, transition: { delay: 1000, duration: 500, type: 'keyframes', ease: 'easeOut' } }">
                            <img class="h-auto max-w-full rounded-lg" src="/images/image-3.jpeg">
                        </div>
                        <div v-motion :initial="{ scale: 0, opacity: 0, }"
                            :enter="{ scale: 1, opacity: 1, transition: { delay: 1500, duration: 500, type: 'keyframes', ease: 'easeOut' } }">
                            <img class="h-auto max-w-full rounded-lg" src="/images/image-4.jpeg">
                        </div>
                    </div>
                </div>
            </div>
            <div class="hidden md:flex md:flex-col md:justify-center h-full">
                <div class="py-2 text-center font-semibold text-base">Highlight Project</div>
                <UCarousel v-slot="{ item }" :items="items" :ui="{ item: 'snap-start' }">
                    <img :src="item" width="300" height="400">
                </UCarousel>
            </div>
        </div>
    </div>
</template>