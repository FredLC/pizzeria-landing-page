<template>
    <carousel :per-page="1" :mouse-drag="true" :paginationEnabled="false">
        <slide v-for="(slide, index) in slides" :key="index">
            <div
                class="slider_bck"
                :style="{ background: `url(${slide.background})` }"
            >
                <div class="container slider-container">
                    <div class="text">
                        <div>{{ slide.text }}</div>
                    </div>
                    <div class="image">
                        <img :src="slide.img" alt="slider image" />
                    </div>
                </div>
            </div>
        </slide>
    </carousel>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
import slideBackground from '../../assets/images/slide_bck.jpg';
import slideBackgroundTwo from '../../assets/images/slide_bck2.jpg';
import pizzaOne from '../../assets/images/pizza_one.png';
import pizzaTwo from '../../assets/images/pizza_three.png';

export default {
    data() {
        return {
            slides: [
                {
                    text: '20% OFF ON ALL PIZZAS',
                    background: slideBackground,
                    img: pizzaOne,
                },
                {
                    text: 'BUY TWO, GET ONE FREE',
                    background: slideBackgroundTwo,
                    img: pizzaTwo,
                },
            ],
        };
    },
    components: {
        Carousel,
        Slide,
    },
};
</script>
