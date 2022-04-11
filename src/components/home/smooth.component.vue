<template>
    <div class="smooth"></div>
</template>

<style scoped>
.smooth {
    width: 100vw;
    position: fixed;
    bottom: 0;
    left: 0;
    height: 80px;
    background-image: linear-gradient(
        to top,
        rgba(255, 255, 255, .5),
        rgba(255, 255, 255, .5),
        rgba(255, 255, 255, .2),
        rgba(255, 255, 255, .1),
        transparent
    )
}
</style>