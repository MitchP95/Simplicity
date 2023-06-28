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
                <li>Currently in Pre-Alpha</li>
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

}

.about-block {
    background: var(--background);
    border-radius: 15px;
    border: solid white 1px;
    width: fit-content;
    height: fit-content;
    margin: 22px;
}

</style>