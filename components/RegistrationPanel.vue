<template>
    <div class="create-account-panel">
        <div class="create-account-panel-top">
            <h1 class="first-title"> 
                HWR Student Portal 
            </h1>
            <img class="bear-image" src="~/assets/images/hwr_bear.png">
            <h2 class="second-title"> 
                Registrierung 
            </h2>
        </div>
        <div class="create-account-panel-middle">
            <v-text-field class="email-create-input"
                hide-details
                single-linenpm 
                filled outlined 
                label="HWR - Emailadresse"
                hint="Deine Emailadresse der bei der HWR">
            </v-text-field>

            <v-text-field class="username-create-input"
                hide-details
                single-linenpm 
                filled outlined 
                label="Benutzername"
                hint="Dein Nutzername von Moodle">
            </v-text-field>
            
            <v-text-field class="password-create-input"
                hide-details
                single-linenpm 
                filled outlined 
                label="Passwort"
                hint="Dein Passwort von Moodle">
                :rules="rules"
            </v-text-field>

            <v-text-field class="password2-create-input"
                hide-details
                single-linenpm 
                filled outlined 
                label="Passwort bestätigen"
                hint="Dein Passwort von Moodle">
            </v-text-field>
        </div>
        <div class="panel-toa">
            <v-checkbox class="panel-toa-checkbox">
                <template v-slot:label>
                    <div>
                        Aktzeptierst du die 
                        <a href="/"> 
                        allgemeinen Geschäftsbedingungen
                        </a> 
                        ?
                    </div>
                </template>    
            </v-checkbox>
            <v-btn  class="continue-button" 
                    to="/" 
                    :disabled="!enabled">
                    Registrieren
            </v-btn>
        </div>
        <div class="create-account-panel-bottom">

        </div>
    </div>
</template>

<style>
.create-account-panel {
    width: 40%;
    height: 100%;
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-self: center;
    border: 1px solid #D50B2E;
    border-radius: 15px;
}

.create-account-panel-top {
    display: flex;
    flex-direction: column;
    align-self: center;
}

.first-title {
    margin-bottom: 40px;
    color: #D50B2E;
}

.bear-image {
    width: 25%;
    height: 40%;
    margin-bottom: 50px;
    align-self: center;
}

.second-title {
    align-self: center;
    margin-bottom: 65px;
}

.create-account-panel-middle {
    display: flex;
    flex-direction: column;
    
}

.email-create-input {
    margin-bottom: 25px !important;
    background-color: #fff;
    border: 1px solid #D50B2E;
}

.username-create-input {
    margin-bottom: 25px !important;
    background-color: #fff;
    border: 1px solid #D50B2E;
}


.password-create-input {
    margin-bottom: 25px !important;
    background-color: #fff;
    border: 1px solid #D50B2E;
}

.password2-create-input {
    margin-bottom: 25px !important;
    background-color: #fff;
    border: 1px solid #D50B2E;
}

.create-account-panel-bottom {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    gap: 2%;
}

.panel-toa{

}

.panel-toa-checkbox{

}


.continue-button {
    width: 49%;
    height: 40px !important
}
</style>

<script>

</script>