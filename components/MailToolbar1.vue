<template>
    <v-row class="mail-toolbar">

        <div class="new">
            <v-dialog v-model="dialog" persistent width="1024">
                <template v-slot:activator="{ props }">
                    <v-btn v-bind="props" @click="dialog = true">
                        <v-icon>mdi-file-plus @click="dialog = true"</v-icon>Verfassen
                    </v-btn>
                </template>
                <v-card>
                    <v-card-title>
                        <div class="emailTitle">EMAIL VERFASSEN</div>
                    </v-card-title>
                    <v-card-text>
                        <v-container>
                            <template>
                                <div class="container">
                                    <form @submit.prevent="saveData()">
                                        <form @submit.prevent="sendEmail">
                                            <label>An*</label>
                                            <input type="email" v-model="email" name="An" placeholder="jeanette.paetzoldt@hwr-berlin.de" />

                                            <label>CC</label>
                                            <input type="email" v-model="cc" name="email" placeholder="CC" />

                                            <label>Betreff*</label>
                                            <input type="text" v-model="name" name="Betreff" placeholder="Betreff" />

                                            <label>Nachricht*</label>
                                            <textarea name="Nachricht" v-model="message" cols="30" rows="5"
                                                placeholder="Nachricht">
                                                              </textarea>

                                            <input type="submit" value="Senden" />
                                        </form>
                                    </form>
                                    <small>*Pflichtfelder</small>
                                </div>
                            </template>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn color="blue-darken-1" variant="text" @click="dialog = false">
                                    Verwerfen
                                </v-btn>
                                <v-btn color="blue-darken-1" variant="text" @click="dialog = false">
                                    Speichern
                                </v-btn>
                            </v-card-actions>
                        </v-container>
                    </v-card-text>
                </v-card>
            </v-dialog>
        </div>
        <div>
            <v-btn variant="flat"><v-icon>mdi-folder-zip</v-icon> Archivieren
            </v-btn>
        </div>
        <div>
            <v-btn variant="tonal"><v-icon>mdi-delete-forever</v-icon>Löschen</v-btn>
        </div>

    </v-row>
</template>

<script>
export default {
    data: () => ({
        name: "",
        email: "",
        cc: "",
        message: "",
        dialog: false,

        items: [
            {
                title: "Klick mich"
            },
            {
                title: "Klick mich"
            },
            {
                title: "Klick mich"
            },
            {
                title: "Klick mich"
            }
        ],
        select: [
            {
                text: "Status 1"
            },
            {
                text: "Status 2"
            },
            {
                text: "Status 3"
            },
            {
                text: "Status 4"
            },
            {
                text: "Status 5"
            },
            {
                text: "Status 6"
            },
            {
                text: "Status 7"
            }
        ],

        sendEmail(e) {
            try {
                sendForm(
                    "YOUR_SERVICE_ID",
                    "YOUR_TEMPLATE_ID",
                    e.target,
                    "YOUR_USER_ID",
                    {
                        name: this.name,
                        email: this.email,
                        cc: this.cc,
                        message: this.message
                    }
                );
            } catch (err) {
                if (err instanceof ReferenceError) {
                    alert("JSON Error: " + err.message);
                } else {
                    throw err; // rethrow
                }
            }
            // Reset form field
            this.name = "";
            this.email = "";
            this.cc = "";
            this.message = "";
        }
    })
};
</script>

<style lang="scss">
.mail-toolbar {
    width: 85vw;
    align-self: center;
    margin-left: 2rem;
}

.checkbox-custom {
    width: 2rem;
    height: 2rem;
    float: left;
    margin-right: 2rem;
    margin-top: 0.1rem;
}

.list {
    width: 100px;
    height: 100px;
    display: block;
}

.new {
    margin-right: 5rem;
}

.menu {
    margin-left: 3rem;
}

.toolbar {
    background-color: #363636;
}

.v-btn>.v-btn__content .v-icon {
    font-size: 2.1rem;
    color: #d50b2e;
}

label {
    float: left;
}

input[type="text"],
[type="email"],
textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #f0f0f0;
    border-radius: 4px;
    box-sizing: border-box;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
}

input[type="submit"] {
    background-color: $color-hwr-red;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

input[type="submit"]:hover {
    background-color: #b8c7b9;
}
</style>
