<template>
    <div class="max-h-screen bg-[#DFF8FD] py-8">
        <div class="h-screen">
            <div class="py-2 text-center font-semibold text-base">Highlight Project</div>
            <div class=" grid grid-cols-2 mx-4 gap-0">
                <div class="grid gap-1">
                    <div>
                        <img class="h-auto max-w-[90%] rounded-lg"
                            src="/images/image-1.jpeg">
                    </div>
                    <div>
                        <img class="h-auto max-w-[90%] rounded-lg"
                            src="/images/image-2.jpeg">
                    </div>
                </div>
                <div class="grid gap-1">
                    <div>
                        <img class="h-auto max-w-[90%] rounded-lg"
                            src="/images/image-3.jpeg">
                    </div>
                    <div>
                        <img class="h-auto max-w-[90%] rounded-lg"
                            src="/images/image-4.jpeg">
                    </div>
                </div>

                <div class="grid col-span-2 py-4 text-center">
                    <nuxtLink to="https://github.com/wildy13/">More</nuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>