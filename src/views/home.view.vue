<template>
    <div class="container">
        <Product :image="require('@/assets/test.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test2.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test4.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test5.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test2.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test4.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test5.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test2.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test4.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test5.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test2.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test4.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test5.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test2.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test4.png')" title="Test" description="Teste..." />
        <Product :image="require('@/assets/test5.png')" title="Test" description="Teste..." />
        <Smooth />
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from "vue-property-decorator";
    import Smooth from "@/components/home/smooth.component.vue";
    import Product from "@/components/home/product.component.vue";
    
    @Component({
        components: {
            Product,
            Smooth
        }
    })

    export default class HomeView extends Vue {}
</script>

<style scoped>
.container {
    padding: 30px;
    display: block;
    justify-content: center;
    column-count: 4;
}

@media screen and (max-width: 750px){
    .container {
        column-count: 2;
    }
}
</style>