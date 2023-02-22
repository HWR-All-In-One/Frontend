<template>
    <div>
        <div>
            <v-toolbar class="toolbar" ;>
                <div>
                    <input type="checkbox" v-model="checkAll" class="checkbox-custom" />
                </div>

                <div class="new">
                    <v-btn>
                        <v-icon>
                            mdi-file-plus @click="dialog = true"
                        </v-icon>
                        Verfassen
                    </v-btn>
                </div>

                <v-btn variant="flat">
                    <v-icon>
                        mdi-folder-zip
                    </v-icon>
                    Archivieren
                </v-btn>

                <v-btn variant="tonal">
                    <v-icon>
                        mdi-close-octagon
                    </v-icon>Spam</v-btn>

                <v-btn variant="tonal">
                    <v-icon>
                        mdi-folder-move
                    </v-icon>
                    Verschieben
                </v-btn>

                <v-btn variant="tonal">
                    <v-icon>
                        mdi-delete-forever
                    </v-icon>
                    Löschen
                </v-btn>

                <div class="menu">
                    <v-menu offset-y>
                        <template v-slot:activator="{ on }">
                            <v-btn icon flat v-on="on">
                                <span>
                                    <v-icon>
                                        mdi-dots-vertical
                                    </v-icon></span>
                            </v-btn>
                        </template>
                        <v-list>
                            <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
                                <v-list-tile-title>{{ link.text }}</v-list-tile-title>
                            </v-list-tile>
                        </v-list>
                    </v-menu>
                </div>
            </v-toolbar>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            dialog: false,
            dialog2: false,
            dialog3: false,
            notifications: false,
            sound: true,
            widgets: false,
            items: [
                {
                    title: 'Click Me',
                },
                {
                    title: 'Click Me',
                },
                {
                    title: 'Click Me',
                },
                {
                    title: 'Click Me 2',
                },
            ],
            select: [
                { text: 'State 1' },
                { text: 'State 2' },
                { text: 'State 3' },
                { text: 'State 4' },
                { text: 'State 5' },
                { text: 'State 6' },
                { text: 'State 7' },
            ],
        }
    },
}
</script>

<style>
.checkbox-custom {
    width: 2rem;
    height: 2rem;
    float: left;
}

.list {
    width: 100px;
    height: 100px;
    display: block;
}

.new {
    margin-left: 3rem;
    margin-right: 5rem;
}

.menu {
    margin-left: 5rem;
}

.toolbar {
    background-color: #363636;
}

.v-btn>.v-btn__content .v-icon {
    font-size: 2.1rem;
    color: #d50b2e;
}
</style>
