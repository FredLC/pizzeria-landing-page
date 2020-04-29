<template>
    <div id="app">
        <comp-header />
        <comp-featured />
        <comp-menu />
        <comp-footer />
    </div>
</template>

<script>
import compHeader from './components/Header-Footer/Header';
import compFeatured from './components/Featured/index';
import compMenu from './components/Menu/index';
import compFooter from './components/Header-Footer/Footer';

export default {
    name: 'App',
    components: {
        compHeader,
        compFeatured,
        compMenu,
        compFooter,
    },
};
</script>

<style>
@import './assets/style.css';
</style>
