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
            <v-text-field class="email-create-input" hide-details single-line filled outlined label="HWR - Emailadresse"
                hint="Deine Emailadresse der bei der HWR">
            </v-text-field>

            <v-text-field class="username-create-input" hide-details single-linenpm filled outlined label="Benutzername"
                hint="Dein Nutzername von Moodle">
            </v-text-field>

            <v-text-field class="password-create-input" hide-details single-linenpm filled outlined label="Passwort"
                hint="Dein Passwort von Moodle">
                :rules="rules"
            </v-text-field>

            <v-text-field class="password2-create-input" hide-details single-linenpm filled outlined
                label="Passwort bestätigen" hint="Dein Passwort von Moodle">

            </v-text-field>
        </div>
        <div class="panel-toa">
            <v-checkbox class="panel-toa-checkbox" v-model="toaBoolean"/>
            <div class="agb-container">
                Akzeptierst du die
                <a class="agb-link" href="/">AGB</a>?
            </div>
            <v-btn class="continue-button" id="continueButton" to="/" :disabled="!toaBoolean">
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
    height: 46.5rem;
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
  name: 'App',
  data: () => ({
    toaBoolean: true,
  }),
};

</script>