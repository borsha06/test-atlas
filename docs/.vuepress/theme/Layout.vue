<template>
<div class="theme-container">
    <component class="main-content" :is="layout"/>
</div>
</template>
<script>
    import Vue from 'vue'
    import Va from '../../../node_modules/vue-atlas/src/index.js'
    Vue.use(Va, 'en')
    import home from './layouts/home.vue';
    import post from './layouts/post.vue';


    export default {
            components: {
                'home': home
            },
        computed: {
            layout(){
                const { path } = this.$page;
                if(path === '/')
                {
                    return 'home'
                }
                else
                {
                    return 'post'
                }
            }
        }

    }
</script>