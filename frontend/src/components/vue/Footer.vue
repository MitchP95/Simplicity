<script setup>
const props = defineProps({
    title: String
});
</script>

<template>
    <div class="functional-footer">
        <div class="about-block">
            <ul>
                <li>Designed and built by Mitchell Puersten</li>
                <li>Current in Pre-alpha</li>
                <li>MIT License</li>
            </ul>
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

ul {
    padding: 10px;
    list-style: none;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

li {
    color: var(--text-color);
}

div.functional-footer {
    width: 100vw;
    height: fit-content;
    position: absolute;
    left: 0;
    bottom: 0;
    background: var(--background);
    border-top: solid 1px var(--accent);
}

.about-block {
    background: var(--background);
    border-radius: 15px;
    box-shadow: 0px 4px 10px var(--accent);
    width: fit-content;
    height: fit-content;
    margin-left: 22px;
}

</style>