<script setup>

function launchActivityModal() {
    console.log("Launching modal.");
}

</script>

<template>
    <button @click="launchActivityModal">Add Activity</button>
</template>

<style>
    button {
        background: var(--secondary-background);
        color: var(--text-color);
        font-size: larger;
        font-weight: bold;

        padding: 12px;
        border: none;
        border-radius: 12px;
    }

    button:hover {
        cursor: pointer;
    }
</style>