<template>
    <div class="max-h-screen bg-[#DFF8FD]">
        <div class="h-screen">
            <Navbar />
            <div>
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
        </div>
    </div>
</template>