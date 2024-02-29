<script setup>
const items = [
    {
        key: 'education',
        label: 'Education',
        content: [{
            major: 'Information Technology Engineering',
            university: 'Batam State Polytechnic',
            year: 2024
        }]
    },
    {
        key: 'experiences',
        label: 'Experiences',
        content: [
            {
                role: 'Production Employee',
                company: 'Nok Freudenberg Sealing Technologies',
                from: 'July 2021',
                to: 'July 2022'
            },
            {
                role: 'Intern Web Developer',
                company: 'Labtech International',
                from: 'July 2022',
                to: 'March 2023'
            },
            {
                role: 'Web Developer',
                company: 'Labtech International',
                from: 'April 2023',
                to: 'Now'
            }
        ]
    }
]

const education = reactive()
const experiences = reactive()

</script>


<template>
    <div class="max-h-screen bg-[#DFF8FD]">
        <div class="h-screen">
            <Navbar />
            <div class="flex justify-end w-full">
                <div class="py-16  w-full  flex  justify-end md:justify-evenly space-x-20">
                    <div class="hidden md:block max-w-md">
                        <div v-motion :initial="{ y: -100, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 1200, type: 'keyframes', ease: 'easeOut' } }" class="px-4  py-1 border-b-2 border-[#363030] text-xl">WHAT I DO</div>
                        <div v-motion :initial="{ x: -500, opacity: 0, }"
                        :enter="{ x: 0, opacity: 1, transition: { duration: 1200, type: 'keyframes', ease: 'easeOut' } }" class="px-7 py-2 text-2xl text-justify">
                            As a <span class="text-red-500">web developer</span>, I have a passion for seeking knowledge and
                            experience.
                            can compete with times that are
                            changing too quickly and can work together with a team so that problems can be resolved.
                        </div>
                        <div v-motion :initial="{ x: -500, opacity: 0, }"
                        :enter="{ x: 0, opacity: 1, transition: { duration: 1200, type: 'keyframes', ease: 'easeOut' } }" class="px-7 py-2 text-2xl text-justify">
                            As a <span class="text-red-500">son</span>, I had dreams to make my parents happy so that I
                            could
                            live
                            happily in this world
                        </div>
                    </div>
                    <div v-motion :initial="{ y: -100, opacity: 0, }"
                        :enter="{ y: 0, opacity: 1, transition: { duration: 1200, type: 'keyframes', ease: 'easeOut' } }">
                        <UTabs :items="items" class="w-full px-4">
                            <template #item="{ item }">
                                <UCard @submit.prevent="() => onSubmit(item.key === 'education' ? education : experiences)">
                                    <div v-if="item.key === 'education'" class="space-y-3">
                                        <div v-for="item in item.content">
                                            <div class="text-base font-semibold">
                                                {{ item.major }}
                                            </div>
                                            <div class="flex space-x-4 text-gray-400 text-sm">
                                                <div>
                                                    {{ item.university }}
                                                </div>
                                                <div>{{ item.year }}</div>
                                            </div>
                                        </div>
                                    </div>
                                    <div v-else-if="item.key === 'experiences'" class="space-y-3">
                                        <div v-for="item in item.content">
                                            <div class="text-base font-semibold">
                                                {{ item.role }}
                                            </div>
                                            <div class="text-gray-400 text-sm">
                                                {{ item.company }}
                                            </div>
                                            <div class="text-gray-400 text-sm flex space-x-1">
                                                <span>{{ item.from }}</span>
                                                <span>-</span>
                                                <span>{{ item.to }}</span>
                                            </div>
                                        </div>
                                    </div>
                                </UCard>
                            </template>
                        </UTabs>
                    </div>
                    <div>
                        <img v-motion :initial="{ x: -375, opacity: 0, }"
                            :enter="{ x: 0, opacity: 1, transition: { duration: 1500, type: 'keyframes', ease: 'easeOut' } }"
                            src="/avatar.png" alt="avatar"
                            class="absolute bottom-0 -left-[50%] lg:-left-[35%] xl:-left-[20%] z-50 h-auto">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>