<template>
    <div class="wrap">
        <Header />
        <Link />
        <Nuxt />
        <Footer />
    </div>
</template>

<script>
import Header from "~/components/Header.vue";
import Link from "~/components/Link.vue";
import Footer from "~/components/Footer.vue";
export default {
    components: {
        Header,
        Link,
        Footer
    },
};
</script>

<style>
    #__nuxt,
    #__layout{
        height: 100%;
    }
</style>
