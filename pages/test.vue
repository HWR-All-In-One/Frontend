<template>
    <v-app>
        <div class="main-component">
            <h1 class="main-title">
                Komponentenbibliothek
            </h1>
            <!-- 
                Kopiere dir die Kompenentenvorlage aus dem "Default Component"-Bereich und 
                füge sie in alphabetischer Reihenfolge der Komponentenbibliothek im "Component Library"-Bereich hinzu.
            -->
        </div>        

        <!-- Start of Component Library -->

        <!-- A -->

        <div class="component">
            <h2 class="component-title">
                Pop-Up Meldungen - Alert.vue
            </h2>
            <div class="component-box">
                <Alert/>
            </div>
            <br/>
        </div>


        <!-- B -->



        <!-- C -->



        <!-- D -->



        <!-- E -->



        <!-- F -->

        <div class="component">
            <h2 class="component-title">
                Passwort vergessen Panel  - ForgetPasswordPanel.vue
            </h2>
            <div class="component-box">
                <ForgetPasswordPanel />
            </div>
            <br/>
        </div>



        <!-- G -->



        <!-- H -->



        <!-- I -->



        <!-- J -->



        <!-- K -->



        <!-- L -->



        <!-- M -->

        <div class="component">
            <h2 class="component-title">
                Mail Werkzeugleiste - MailToolbar.vue
            </h2>
            <div class="component-box">
                <MailToolbar />
            </div>
            <br/>
        </div> 

        <div class="component">
            <h2 class="component-title">
                Mail Page Inbox Winter - MailInbox1.vue
            </h2>
            <div class="component-box">
                <MailInbox1/>
            </div>
            <br/>
        </div>

        <div class="component">
            <h2 class="component-title">
                Mail Page Inbox Höhne- MailInbox2.vue
            </h2>
            <div class="component-box">
                <MailInbox2/>
            </div>
            <br/>
        </div>

        


        <!-- N -->



        <!-- O -->

        <div class="component">
            <h2 class="component-title">
                Open Dialog TEST - OpenDialog.vue
            </h2>
            <div class="component-box">
                <OpenDialog/>
            </div>
            <br/>
        </div> 



        <!-- P -->

        <div class="component">
            <h2 class="component-title">
                Passworteingabe - PasswordPanel.vue
            </h2>
            <div class="component-box">
                <PasswordPanel/>
            </div>
            <br/>
        </div> 

        <div class="component">
            <h2 class="component-title">
                Mail Page Pätzoldt Folder - Paetzoldt.vue
            </h2>
            <div class="component-box">
                <Paetzoldt />
            </div>
            <br/>
        </div>
        

        <!-- Q -->



        <!-- R -->

        <div class="component">
            <h2 class="component-title">
                Registrierung - RegistrationPanel.vue
            </h2>
            <div class="component-box">
                <RegistrationPanel />
            </div>
            <br/>
        </div> 

        <!-- S -->

        <div class="component">
            <h2 class="component-title">
                Passwort vergessen Panel  - Setting.vue
            </h2>
            <div class="component-box">
                <Setting />
            </div>
            <br/>
        </div>

        <div class="component">
            <h2 class="component-title">
                Stundenplan - Schedule.vue
            </h2>
            <div class="component-box">
                <Schedule />
            </div>
            <br/>
        </div>

        <div class="component">
            <h2 class="component-title">
                Stundenplan Dropdown-Liste - ScheduleList.vue
            </h2>
            <div class="component-box">
                <ScheduleList />
            </div>
            <br/>
        </div>

        <!-- T -->

        <div class="component">
            <h2 class="component-title">
                Test Komponente - Test.vue
            </h2>
            <div class="component-box">
                <Test />
            </div>
            <br/>
        </div>

        <!-- U -->

        <div class="component">
            <h2 class="component-title">
                Benutzerkonto Anmeldepanel Nr. 1 - UsernamePanel.vue
            </h2>
            <div class="component-box">
                <UsernamePanel />
            </div>
            <br/>
        </div>

        <!-- V -->



        <!-- W -->



        <!-- X -->



        <!-- Y -->



        <!-- Z -->



        <!-- End of Component Library -->

        <div class="main-component">
            <h1 class="main-title">
                Komponentenvorlage
            </h1>
        </div>

        <!-- Default Component - Do not delete !!! -->

        <div class="component">
            <h2 class="component-title">
                Titel der Komponente
                <!-- 
                    Besteht aus der deutschen Komponentenbezeichnung und dem Vue-Dateinamen
                    Beispiel: Stundenplan - Schedule.vue 
                -->
            </h2>
            <div class="component-box">
                Tag zur Komponente
                <!-- 
                    Vergiss nicht die Komponente im Script zu importieren
                -->
            </div>
            <br/>
        </div>
        
        <!-- End of Default Component -->
    </v-app>
</template>
  
<script>
import Alert from '~/components/Alert.vue';
import ForgetPasswordPanel from '~/components/ForgetPasswordPanel.vue';
import MailToolbar from '~/components/MailToolbar.vue';
import PasswordPanel from '~/components/PasswordPanel.vue';
import RegistrationPanel from '~/components/RegistrationPanel.vue';
import Schedule from '~/components/Schedule.vue';
import ScheduleList from '~/components/ScheduleList.vue';
import Test from '~/components/Test.vue';
import UsernamePanel from '~/components/UsernamePanel.vue';
import Setting from '~/components/Setting.vue';
import MailInbox1 from '~/components/MailInbox1.vue';
import MailInbox2 from '~/components/MailInbox2.vue';
import MailInbox3 from '~/components/MailInbox3.vue';
import OpenDialog from '~/components/OpenDialog.vue';


export default {
    name: "TestLayout",
    components: {
    Alert,
    PasswordPanel,
    RegistrationPanel,
    Schedule,
    ScheduleList,
    UsernamePanel,
    ForgetPasswordPanel,
    Test,
    MailToolbar,
    Setting,
    MailInbox1,
    MailInbox2,
    MailInbox3,
    
    OpenDialog
}
}
</script>

<style lang="scss">
/* Dark Theme Styling */


/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.main-component {
    display: flex;
    flex-direction: column;
    width: 100%;
}

.main-title,
.component-main-title {
    padding: 30px 0 30px 0;
}

.component-title {
    padding-bottom: 10px;
    text-align: center;
    padding-top: 10px;
    color: $color-dark-mode-grey;
}

.component {
    display: flex;
    margin-bottom: 30px;
    background-color: white;
    border-radius: 30px;
    flex-direction: column;
    width: 100%;
}

.component:last-child {
    margin-bottom: 30px;
}

.component-box {
    width: 90%;
    margin-left: 5%;
    text-align: center;
    color: $color-dark-mode-grey;
}
</style>