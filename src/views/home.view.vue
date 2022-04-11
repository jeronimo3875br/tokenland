<template>
    <div class="container">
        {{ pushImages() }}
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
        private readonly sources: string[] = [
            require('@/assets/test.png'),
            require('@/assets/test2.png'),
            require('@/assets/test4.png'),
            require('@/assets/test5.png')
        ]

        private titles: string[] = [
            "Pedro",
            "Bruno",
            "Marcos",
            "Armando",
            "Paulo",
            "Jeronimo"
        ]

        private readonly images: IImages[] = []

        private pushImages(): void {
            for (let i = 0; i < 10; i++){
                this.images.push({
                    title: this.titles[Math.floor(Math.random() * this.titles.length)],
                    source: this.sources[Math.floor(Math.random() * this.sources.length)],
                    description: "Teste..."
                })
            }
        }
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