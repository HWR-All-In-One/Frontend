<template>
    <div class="login-panel">
        <div class="login-panel-top">
            <h1 class="first-title">
                HWR Student Portal
            </h1>
            <img class="bear-image" src="~/assets/images/Bear.png">
            <h2 class="second-title">
                Anmeldung
            </h2>
            <h3 class="third-title">
                Zum Benutzerkonto
            </h3>
        </div>
        <div class="login-panel-middle">
            <v-text-field class="username-input"
                hide-details
                single-linenpm
                filled outlined
                label="Benutzer"
                hint="Dein Nutzername von Moodle">
            </v-text-field>
            <a class="forgot-user-link" href="https://www.it.hwr-berlin.de/helpdesk/formulare/">
                Benutzernamen vergessen?
            </a>
        </div>
        <div class="login-panel-bottom">
            <v-btn class="create-account-button" secondary to="/registration">
                Konto erstellen
            </v-btn>
            <v-btn class="continue-button" to="/mail" >
                Bestätigen
            </v-btn>
        </div>
    </div>
</template>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark.v-label {
    color: $color-dark-mode-grey;
}

.theme--dark.login-panel {
    border: 1px solid #00ff37 !important;
}

/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.login-panel {
    width: 30rem;
    height: 35rem;
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-self: center;
    border: 1px solid $color-hwr-red;
    border-radius: 15px;
}

.login-panel-top {
    display: flex;
    flex-direction: column;
    align-self: center;
}

.first-title {
    margin-bottom: 1rem;
    font-size: 30px;
    color: $color-hwr-red;
}

.bear-image {
    width: 6rem;
    height: 6rem;
    margin-bottom: 1rem;
    align-self: center;
}

.second-title {
    align-self: center;
    margin-bottom: 1rem;
}

.third-title {
    align-self: center;
    margin-bottom: 2rem;
}

.login-panel-middle {
    display: flex;
    flex-direction: column;
    background-color: #fff;
}

.username-input {
    background-color: $color-white;
    border: 1px solid $color-hwr-red;
}

.forgot-user-link {
    margin-top: 10px;
    margin-bottom: 30px;
}

.login-panel-bottom {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 2%;
}

.create-account-button {
    width: 49%;
    border: 1px solid $color-hwr-red !important;
}

.continue-button {
    width: 49%;
    border: 1px solid $color-hwr-red !important;
}
</style>
