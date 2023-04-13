<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppSeller from './components/AppSeller.vue';
import AppFooter from './components/AppFooter.vue';

export default {
    components: {
        AppHeader,
        AppContent,
        AppSeller,
        AppFooter
    }
}
</script>

<template>
    <AppHeader />
    <AppContent />
    <AppSeller />
    <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>