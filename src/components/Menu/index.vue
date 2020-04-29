<template>
    <div class="container menu_container">
        <div class="top">
            <h2>Menu</h2>
        </div>
        <div class="buttons">
            <md-button
                v-for="(button, index) in buttons"
                :key="index"
                :class="button.active ? 'md-raised' : ''"
                @click="changeMenu(button.name)"
            >
                {{ button.name }}
            </md-button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            buttons: [
                { name: 'pizzas', active: true },
                { name: 'burgers', active: false },
                { name: 'salads', active: false },
                { name: 'desserts', active: false },
            ],
            products: [],
        };
    },
    methods: {
        changeMenu(value) {
            this.buttons.forEach((item) => {
                if (item.name === value) {
                    item.active = true;
                } else {
                    item.active = false;
                }
            });
        },
    },
    created() {
        this.$http
            .get('products.json')
            .then((response) => response.json())
            .then((data) => {
                let list = [];

                for (let key in data) {
                    list.push({
                        ...data[key],
                        id: key,
                    });
                }
                this.products = list;
            });
    },
};
</script>
