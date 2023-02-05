<template>
    <div class="login-panel">
        <div class="login-panel-top">
            <h1 class="first-title"> 
                HWR Student Portal 
            </h1>
            <img class="bear-image" src="~/assets/images/hwr_bear.png">
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
            <a class="forgot-user-link" href="/">
                Benutzer vergessen?
            </a>
        </div>
        <div class="login-panel-bottom">
            <v-btn class="create-account-button" secondary to="/">
                Konto erstellen
            </v-btn>
            <v-btn class="continue-button">
                Bestätigen
            </v-btn>
        </div>
    </div>
</template>

<style>
.login-panel {
    width: 50%;
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-self: center;
    border: 1px solid #D50B2E;
    border-radius: 15px;
}

.login-panel-top {
    display: flex;
    flex-direction: column;
    align-self: center;
}

.first-title {
    margin-bottom: 30px;
    color: #D50B2E;
}

.bear-image {
    width: 25%;
    height: 45%;
    margin-bottom: 30px;
    align-self: center;
}

.second-title {
    align-self: center;
    margin-bottom: 15px;
}

.third-title {
    align-self: center;
    margin-bottom: 30px;
}

.login-panel-middle {
    display: flex;
    flex-direction: column;
}

.username-input {
    background-color: #fff;
}

.forgot-user-link {
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
    color: #D50B2E;
}

.continue-button {
    width: 49%;
}
</style>