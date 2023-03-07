

<template>

    <div class="new">
      <v-dialog v-model="dialog" persistent width="1024">
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props" @click="dialog = true">
            Übungsblatt
          </v-btn>
        </template>
        <v-card>
          <v-card-title>
            <div class="emailTitle">E-Mail</div>
          </v-card-title>
          <v-card-text>
            <v-container>
              <template>
                <div>

                  <v-card class="mx-auto" max-width="100%">
                    <v-card-text>
                      <p class="textSubject">
                        21004262 IT1151 FS 4 TIT21A: 4. Übungsblatt
                      </p>
                      <p class="textSubject">
                        von <strong>Nicola Winter</strong> Freitag, 24. Februar
                        2023, 14:53 PM
                      </p>
                      <p class="normal">Liebe Studierende der Informatik,</p>
                      <p class="normal">
                        im Moodle steht das 4. Übungsblatt für Sie bereit.
                      </p>
                      <p class="normal">Viel Spaß beim Lösen der Aufgaben!</p>
                      <p class="normal">
                        Den Artikel zum Algorithmus der Woche für das Max Flow
                        Problem finden Sie unter folgendem Link:
                        <a
                          href="https://algo.rwth-aachen.de/~algorithmus/algo23.php"
                          >https://algo.rwth-aachen.de/~algorithmus/algo23.php</a
                        >
                      </p>
                      <p class="normal">
                        Mit freundlichen Grüßen <br />
                        Prof. Dr. Nicola Winter <br />
                        Hochschule für Wirtschaft und Recht Berlin<br />
                        Fachbereich 2 <br />
                        Alt-Friedrichsfelde 60 <br />
                        D-10315 Berlin <br />
                        E-Mail:<a href="nicola.winter@hwr-berlin.de"
                          >nicola.winter@hwr-berlin.de</a
                        >
                      </p>
                    </v-card-text>
                  </v-card>
                </div>
              </template>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                  color="blue-darken-1"
                  variant="text"
                  @click="dialog = false"
                >
                  Schließen
                </v-btn>
                <v-btn
                  color="blue-darken-1"
                  variant="text"
                  @click="dialog = false"
                >
                  Antworten
                </v-btn>
              </v-card-actions>
            </v-container>
          </v-card-text>
        </v-card>
      </v-dialog>
    </div>
</template>

<script>
export default {
  data: () => ({
    dialog: false
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

.v-btn > .v-btn__content .v-icon {
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
  border: 1px solid #ccc;
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
