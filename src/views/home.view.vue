<template>
    <div class="container">
        <Product 
            v-for="image in images" 
            :key="image" 
            :image="image.source" 
            :title="image.title" 
            description="Teste..." 
        />
        <Smooth />
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from "vue-property-decorator";
    import Smooth from "@/components/home/smooth.component.vue";
    import Product from "@/components/home/product.component.vue";

    interface IImages {
        title: string;
        source: string;
        description: string;
    }
    
    @Component({
        components: {
            Product,
            Smooth
        }
    })

    export default class HomeView extends Vue {
        private readonly images: IImages[] = [
            { title: "Macaco", source: require('@/assets/test.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test2.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test4.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test5.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test2.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test4.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test5.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test2.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test4.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test5.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test2.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test4.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test5.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test2.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test4.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test5.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test2.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test4.png'), description: "Teste..." },
            { title: "Macaco", source: require('@/assets/test5.png'), description: "Teste..." },
        ]
    }
</script>

<style scoped>
.container {
    padding: 10px;
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