<template>
    <a class="title">{{ title }}</a>
</template>

<script lang="ts">
    import { Vue, Component, Prop } from "vue-property-decorator";

    @Component
    export default class TitleComponent extends Vue {
        @Prop()
        private title = "";
    }
</script>

<style scoped>
.title {
    color: #646060;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.6rem;
    cursor: pointer;
    font-family: 'Amaranth', sans-serif;
}
</style>