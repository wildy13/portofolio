<script setup>
const waiting = ref(false);


const form = ref({
    name: '',
    email: '',
    subject: '',
    message: ''
})

const submit = (form) => {
    waiting.value = true;
    window.open(`mailto:wildy.simanjuntak13@gmail.com?subject=${form.subject}&&body=${form.message}`)
}
</script>




<template>
    <div class="max-h-screen bg-[#DFF8FD]">
        <div class="h-screen">
            <Navbar />
            <div v-motion :initial="{ scale: 0 , opacity: 0, }"
                :enter="{ scale: 1, opacity: 1, transition: { duration: 1200, type: 'keyframes', ease: 'easeOut' } }"
                class="h-screen w-full flex flex-col items-center justify-center pb-16">
                <div>
                    <div class="text-center text-base font-bold">Get in touch</div>
                    <div class="font-semibold text-sm text-center">For inquiries regarding my portfolio, please feel free to
                        reach out.</div>
                </div>
                <form @submit.prevent="submit(form)" class="w-full max-w-xs md:max-w-4xl text-sm">
                    <div class="flex flex-col px-7l">
                        <div>
                            <div>
                                <label for="name" class="block mb-2 font-semibold">Full Name</label>
                                <input type="text" id="name" class=" text-gray-400  rounded-lg block w-full p-2.5"
                                    placeholder="John" required v-model="form.name">
                            </div>
                        </div>
                        <div>
                            <label for="email" class="block mb-2 font-semibold">Email</label>
                            <input type="email" id="email" class=" text-gray-400  rounded-lg block w-full p-2.5"
                                placeholder="Jhon@example.com" required v-model="form.email">
                        </div>
                        <div>
                            <label for="subject" class="block mb-2 font-semibold">Subject</label>
                            <input id="subject" class=" text-gray-400  rounded-lg block w-full p-2.5" placeholder="Subject"
                                required v-model="form.subject">
                        </div>
                        <div>
                            <label for="message" class="block mb-2 font-semibold">Message</label>
                            <textarea name="message" id="message" rows="4" class="w-full rounded-lg text-gray-400 p-2.5"
                                placeholder="How can i help you?" required v-model="form.message"></textarea>
                        </div>
                        <div class="w-full flex  justify-center">
                            <button type="submit" class="w-32 py-1 rounded-lg hover:transition-colors">
                                <template v-if="waiting">
                                    loading...
                                </template>
                                <template v-if="!waiting">
                                    Send
                                </template>
                            </button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>