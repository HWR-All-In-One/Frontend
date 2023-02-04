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
                Dropdown List - Alert.vue
            </h2>
            <div class="component-box">
                <Alert/>
            </div>
            <br/>
        </div>


        <!-- B -->



        <!-- C -->



        <!-- D -->

        
        <div class="component">
            <h2 class="component-title">
                Dropdown List - DropdownList.vue
            </h2>
            <div class="component-box">
                <DropdownList/>
            </div>
            <br/>
        </div>


        <!-- E -->



        <!-- F -->



        <!-- G -->



        <!-- H -->



        <!-- I -->



        <!-- J -->



        <!-- K -->



        <!-- L -->



        <!-- M -->



        <!-- N -->



        <!-- O -->



        <!-- P -->



        <!-- Q -->



        <!-- R -->



        <!-- S -->

        <div class="component">
            <h2 class="component-title">
                Stundenplan - Schedule.vue
            </h2>
            <div class="component-box">
                <Schedule/>
            </div>
            <br/>
        </div>

        <!-- T -->



        <!-- U -->



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
import Schedule from '~/components/Schedule.vue';

export default {
    name: "TestLayout",
    components: { 
        Schedule
    }
}
</script>

<style>
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
    color: black;
}

.component {
    display: flex;
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
    color: black;
}
</style>