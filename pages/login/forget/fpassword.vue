<template>
    <ForgetPasswordPanel/>
</template>

<script>
import ForgetPasswordPanel from '~/components/ForgetPasswordPanel.vue';
import UsernameField from '~/components/UsernamePanel.vue';

export default {
    name: "DefaultLayout",
    data() {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            items: [
                {
                    icon: "mdi-apps",
                    title: "Welcome",
                    to: "/"
                },
                {
                    icon: "mdi-chart-bubble",
                    title: "Inspire",
                    to: "/inspire"
                }
            ],
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: "Vuetify.js"
        };
    },
    components: { UsernameField, ForgetPasswordPanel }
}
</script>

<style lang="scss">
/* Dark Theme Styling */


/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */

</style>