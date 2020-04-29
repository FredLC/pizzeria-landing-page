<template>
    <div id="app">
        <comp-header />
        <div>
            <md-button>content</md-button>
        </div>
        <comp-footer />
    </div>
</template>

<script>
import compHeader from './components/Header-Footer/Header';
import compFooter from './components/Header-Footer/Footer';

export default {
    name: 'App',
    components: {
        compHeader,
        compFooter,
    },
};
</script>

<style>
@import './assets/style.css';
</style>
