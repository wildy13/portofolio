<template>
    <div class="min-h-screen bg-[#DFF8FD] py-12">
        <div class="h-screen">
            <div class="py-2 text-center font-semibold text-base">Highlight Project</div>
            <div class=" grid grid-cols-2 mx-2 gap-2">
                <div class="grid gap-1">
                    <div>
                        <img class="h-auto max-w-full rounded-lg" src="/images/image-1.jpeg">
                    </div>
                    <div>
                        <img class="h-auto max-w-full rounded-lg" src="/images/image-2.jpeg">
                    </div>
                </div>
                <div class="grid gap-1">
                    <div>
                        <img class="h-auto max-w-full rounded-lg" src="/images/image-3.jpeg">
                    </div>
                    <div>
                        <img class="h-auto max-w-full rounded-lg" src="/images/image-4.jpeg">
                    </div>
                </div>

                <div class="grid col-span-2 py-4 text-center">
                    <div>
                        <nuxtLink to="https://github.com/wildy13/">More</nuxtLink>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>