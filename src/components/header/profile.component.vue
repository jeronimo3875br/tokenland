<template>
    <div class="container">
        <a class="name" v-if="username">{{ username }}</a>
        <div class="profile"></div>
    </div>
</template>

<script lang="ts">
    import { Vue, Component, Prop } from "vue-property-decorator";

    @Component
    export default class ProfileComponent extends Vue {
        @Prop()
        private username = "";
    }
</script>

<style scoped>
.container {
    display: flex;
    align-items: center;
}

.profile {
    cursor: pointer;
    background-color: var(--secondary);
    border: 2px solid var(--tertiary);
    border-radius: 50%;
    cursor: pointer;
    height: 45px;
    width: 45px;
}

.name {
    color: #808080;
    font-size: 20px;
    margin-right: 5px;
    font-family: 'Fira Sans', sans-serif;
    cursor: pointer;
}
</style>