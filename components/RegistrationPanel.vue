<template>
    <div class="create-account-panel">
        <div class="create-account-panel-top">
            <h1 class="first-title">
                HWR Student Portal
            </h1>
            <img class="bear-image" src="~/assets/images/Bear.png">
            <h2 class="second-title">
                Registrierung
            </h2>
        </div>
        <div class="create-account-panel-middle">
            <v-form @submit.prevent>
                <v-text-field class="email-create-input" id="Input1" hide-details single-linenpm filled outlined
                    :rules="rules" name="email" type="email" label="HWR - Emailadresse"
                    hint="Deine Emailadresse der bei der HWR">
                </v-text-field>

                <v-text-field class="username-create-input" id="Input2" hide-details single-linenpm filled outlined
                    name="user" type="user" label="Benutzername" hint="Dein Nutzername von Moodle">
                </v-text-field>

                <v-text-field class="password-create-input" id="Input3" hide-details single-linenpm filled outlined
                    name="password" type="password" label="Passwort" hint="Dein Passwort von Moodle">
                    :rules="rules"
                </v-text-field>

                <v-text-field class="password2-create-input" id="Input4" hide-details single-linenpm filled outlined
                    label="Passwort bestätigen" hint="Dein Passwort von Moodle">

                </v-text-field>
            </v-form>
        </div>
        <div>
            <Mainlist />
        </div>
        <div class="panel-toa">
            <v-checkbox id="checkbox" class="panel-toa-checkbox" />
            <div class="agb-container">
                Akzeptierst du die
                <a class="agb-link" href="/">AGB</a>?
            </div>
            <v-btn class="continue-button" to="/" :disabled="!enabled" id="submit" onclick="registrate()">
                Registrieren
            </v-btn>
        </div>
        <div class="create-account-panel-bottom">
        </div>
</div>
</template>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark.v-label {
    color: $color-dark-mode-grey;
}

.theme--dark.agb-container {
    color: $color-white !important;
}

/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.create-account-panel {
    width: 30rem;
    height: 48.5rem;
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-self: center;
    border: 1px solid $color-hwr-red;
    border-radius: 15px;
}

.create-account-panel-top {
    display: flex;
    flex-direction: column;
    align-self: center;
}

.first-title {
    margin-bottom: 1rem;
    color: $color-hwr-red;
}

.bear-image {
    width: 25%;
    height: 40%;
    margin-bottom: 1rem;
    align-self: center;
}

.second-title {
    align-self: center;
    margin-bottom: 2rem;
}

.create-account-panel-middle {
    display: flex;
    flex-direction: column;
}

.email-create-input {
    margin-bottom: 25px !important;
    background-color: $color-white;
    border: 1px solid $color-hwr-red;
}

.username-create-input {
    margin-bottom: 25px !important;
    background-color: $color-white;
    border: 1px solid $color-hwr-red;
}

.password-create-input {
    margin-bottom: 25px !important;
    background-color: $color-white;
    border: 1px solid $color-hwr-red;
}

.password2-create-input {
    background-color: $color-white;
    border: 1px solid $color-hwr-red;
}

.create-account-panel-bottom {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    gap: 2%;
}

.continue-button {
    width: 49%;
    height: 40px !important;
}

.panel-toa {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}

.agb-container {
    align-self: center;
}
</style>

<script>
export default {
    el: '#checkbox',
    name: 'ContactForm',
    data() {
        return {
            form: {
                name: "",
                email: "",
                message: "",
            },
        };
    },

    methods: {
        enabled() {
            return (
                this.user_name != '' &&
                this.email != '' &&
                this.phone != '' &&
                this.address != ''
            )
        },


        registrate() {

        }
    }

}
    //alert('Halo Welt');
    //name: 'ContactForm',
    //data() {
    //    return {
    //        form: {
    //            name: "",
    //            email: "",
    //            message: "",
    //        },
    //    };
    //},
    //document.getElementById("Input1").style.color ="red";

</script>