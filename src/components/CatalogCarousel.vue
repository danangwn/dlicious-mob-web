<script setup lang="ts">
</script>

<template>
    <div class="row">
        <div class="col">
            <Carousel :itemsToShow="3" :wrapAround="true" :transition="500">
                <Slide v-for="slide in 5" :key="slide">
                    <span class="border rounded">
                        <img src="../../public/banner1.jpg" class="card-img-top" alt="...">
                        <div>
                            <p>Some quick example</p>
                        </div>
                    </span>
                </Slide>
            </Carousel>
        </div>
    </div>
</template>
  
<script>
import { defineComponent } from 'vue'
import { Carousel, Pagination, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
    name: 'Autoplay',
    components: {
        Carousel,
        Slide,
        Pagination,
    },
})
</script>
  
<style scoped>
.carousel__slide {
    padding: 5px;
}

.carousel__viewport {
    perspective: 2000px;
}

.carousel__track {
    transform-style: preserve-3d;
}

.carousel__slide--sliding {
    transition: 0.5s;
}

.carousel__slide {
    opacity: 0.9;
    transform: rotateY(-10deg) scale(0.9);
}

.carousel__slide--active~.carousel__slide {
    transform: rotateY(10deg) scale(0.9);
}

.carousel__slide--prev {
    opacity: 1;
    transform: rotateY(-10deg) scale(0.95);
}

.carousel__slide--next {
    opacity: 1;
    transform: rotateY(10deg) scale(0.95);
}

.carousel__slide--active {
    opacity: 1;
    transform: rotateY(0) scale(1.1);
}
</style>
  
