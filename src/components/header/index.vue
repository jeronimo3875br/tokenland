<template>
    <header>
        <Title title="Tokenland" />
        <!-- <Profile username="Gabriel Jeronimo"  /> -->
    </header> 
</template>

<script>
    import { Vue, Component } from "vue-property-decorator";
    import Title from "@/components/header/title.component.vue";
    import Profile from "@/components/header/profile.component.vue";

    @Component({
        components: {
            Title,
            Profile
        },
    })

    export default class HeaderComponent extends Vue {}
</script>

<style scoped>
header {
    padding: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: var(--primary);
    box-shadow: 0px 0px 10px rgb(0 0 0 / 10%);
}
</style>