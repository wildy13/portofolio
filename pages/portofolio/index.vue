<template>
    <div class="min-h-screen bg-[#DFF8FD] py-8">
        <div class="h-screen">
            <div class="py-2 text-center font-semibold text-base">Highlight Project</div>
            <div class=" grid grid-cols-2 mx-2 gap-2">
                <div class="grid gap-2">
                    <div>
                        <img class="h-auto max-w-full rounded-lg"
                            src="/images/image-1.jpeg" alt="">
                    </div>
                    <div>
                        <img class="h-auto max-w-full rounded-lg"
                            src="/images/image-2.jpeg" alt="">
                    </div>
                </div>
                <div class="grid gap-2">
                    <div>
                        <img class="h-auto max-w-full rounded-lg"
                            src="/images/image-3.jpeg" alt="">
                    </div>
                    <div>
                        <img class="h-auto max-w-full rounded-lg"
                            src="/images/image-4.jpeg" alt="">
                    </div>
                </div>

                <div class="grid col-span-2 py-4 text-center">
                    <nuxtLink to="https://github.com/wildy13/">More</nuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>