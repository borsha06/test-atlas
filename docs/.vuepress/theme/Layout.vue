<template>
    <div>
        <header class="hero is-primary">
            <div class="hero-body">
                <div class="container">
                    <h1 class="title va-btn-primary" >{{ $site.title }}</h1>
                </div>
            </div>
        </header>
        <section class="section">
            <div class="container">
                <Index v-if="isIndex" />
                <Single v-if="!isIndex" />
            </div>
        </section>
    </div>
</template>
<script>
    import Vue from 'vue'
    import Va from '../../../node_modules/vue-atlas/src/index.js'
    Vue.use(Va, 'en')
    import Index from './Index';
    import Single from './Single';
    export default {
        components: {
            Index,
            Single
        },
        computed: {
            isIndex() {
                return this.$page.path.endsWith("/");
            }
        },

    };

</script>
