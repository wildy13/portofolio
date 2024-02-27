<template>
    <Transition>
        <div class="icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-6 h-6 text-blue-500">
                <circle cx="12" cy="12" r="10" color="text-blue-500" />
            </svg>
        </div>
    </Transition>
</template>

<style>
.icon {
    width: 24px;
    height: 24px;
    position: relative;
    animation: float 3s infinite alternate;
}

@keyframes float {
    0% {
        transform: translateY(0);
    }

    100% {
        transform: translateY(-20px);
    }
}

.icon-enter-active,
.icon-leave-active {
    transition: opacity 0.5s;
}

.icon-enter,
.icon-leave-to {
    opacity: 0;
}
</style>