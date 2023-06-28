<script setup>
import { useRouter } from 'vue-router'

const router = useRouter();
const props = defineProps({
    title: String,
});

function navigateToHome() {
    console.log("Called.");
}
</script>

<template>
    <div class="functional-header">
        <div class="title-block" @click="navigateToHome">
            <h1 class="title">{{ props.title }}</h1>
        </div>
    </div>
</template>
<style>
h1 {
    color: var(--text-color);
}

h1.title {
    padding: 10px 20px 12px 20px;
}

div.functional-header {
    width: 100vw;
    height: fit-content;
    position: absolute;
    left: 0;
    top: 0;
    background: var(--secondary-background);
    border-bottom: solid 1px var(--accent);
}

.title-block {
    background: var(--background);
    border-radius: 15px;
    box-shadow: 0px 4px 10px var(--accent);
    width: fit-content;
    height: fit-content;
    margin-left: 22px;
}

.title-block:hover {
    cursor: pointer;
    transform: scale(1.1); /* Scale the whole block on hover */
    transition: transform 0.3s ease-in-out; /* Smoother scaling effect */
}

.title-block:hover h1.title {
    animation: shake 0.25s cubic-bezier(.36,.07,.19,.97) both; /* Apply shaking effect to the text */
    transform: translate3d(0, 0, 0);
    backface-visibility: hidden;
    perspective: 1000px;
}

/* Define shaking animation */
@keyframes shake {
    10%, 90% {
        transform: translate3d(-1px, 0, 0);
    }
    
    20%, 80% {
        transform: translate3d(2px, 0, 0);
    }

    30%, 50%, 70% {
        transform: translate3d(-3px, 0, 0);
    }

    40%, 60% {
        transform: translate3d(3px, 0, 0);
    }
}
</style>