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
    window.open(`mailto:wildy13.simanjuntak13@gmail.com?subject=${form.subject}&&body=${form.message}`)
}
</script>

<template>
    <div class="max-h-screen bg-[#DFF8FD] ">
        <div class="h-screen flex flex-col pt-32">
            <form @submit.prevent="submit(form)" class="pt-2">
                <div class="flex flex-col px-7 space-y-2">
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
</template>