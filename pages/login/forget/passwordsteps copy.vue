<template>
 
 <ForgetPasswordInstructions/>
    
</template>

<script>
import ForgetPasswordInstructions from '~/components/ForgetPasswordInstructions.vue';

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
    components: { UsernameField, ForgetPasswordPanel, ForgetPasswordInstructions }
}
</script>
