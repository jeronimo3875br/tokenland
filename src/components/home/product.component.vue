<template>
    <div class="card">
        <abbr :title="title">
            <img class="product" :src="image" :alt="image" />
        </abbr>
    </div>
</template>

<script lang="ts">
    import { Vue, Component, Prop } from "vue-property-decorator";

    @Component
    export default class ProductComponent extends Vue {
        @Prop()
        private image = "";

        @Prop()
        private title = "";

        @Prop()
        private description = "";
    }
</script>

<style scoped>
.card {
    max-width: 100%;
    box-shadow: 0px 0px 10px rgb(0 0 0 / 10%);
    border-radius: 5px;
    cursor: pointer;
    transition: .3s;
    break-inside: avoid-column;
    border-radius: 3%;
}

.product {
    object-fit: cover;
    width: 100%;
    border-radius: 3%;
}
</style>