<template>
  <div class="main-mail-content">
    <div class="left-mail-content">
      <div class="head">
        <h1 class="page-title">Mails</h1>
        <MailToolbar />
      </div>

      <div>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
                    <v-list-item-action>
                            {{ item.title }}
                    </v-list-item-action>
                </v-list-item>
    </div>

      <div class="mails">
        <div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject1"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Übungsblatt

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Nicola Winter</div>
          <div class="mail-date">01.03.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            AW: Studienprojekt I, 4.Sem., IT21

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Monett Diaz, Dagmar</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Monett Diaz, Dagmar</div>
          <div class="mail-date">01.03.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Übungsblatt

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Jonas Brunkow</div>
          <div class="mail-date">28.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            AW: Studienprojekt - LoRaWAN

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Monett Diaz, Dagmar</div>
          <div class="mail-date">28.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject1"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Übungsblatt

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Nicola Winter</div>
          <div class="mail-date">23.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject1"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Übungsblatt

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Jonas Brunkow</div>
          <div class="mail-date">22.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            4-3161-TIT21 Studienprojekt: Projektpräsentationen - Besprechungsbedarf?

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Monett Diaz, Dagmar</div>
          <div class="mail-date">22.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Jonas Brunkow hat Ihnen für Ihre Lösung bei 'Aufgabe 2: Erstellen sie ein Layout mit CSS' ein Feedback gegeben.

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Jonas Brunkow</div>
          <div class="mail-date">20.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject1"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            21004248 IT3131 FS 4 TIT21A: Hochladen jetzt gruppenweise möglich

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Jonas Brunkow</div>
          <div class="mail-date">17.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject1"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            C++ Aufgabe

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Peter Puschmann </div>
          <div class="mail-date">15.02.23</div>
        </div>


		<div class="single-mail">
          <input
            type="checkbox"
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Aufgabe hochladen

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Peter Puschmann </div>
          <div class="mail-date">15.02.23</div>
        </div>



		<div class="single-mail">
          <input
            type="checkbox"
            
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject1"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Übungsblatt

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Nicola Winter</div>
          <div class="mail-date">13.02.23</div>
        </div>
		<div class="single-mail">
          <input
            type="checkbox"
            
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Übungsblatt

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Nicola Winter</div>
          <div class="mail-date">13.02.23</div>
        </div>
		<div class="single-mail">
          <input
            type="checkbox"
            
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            21004252 IT3131 FS 4 TIT21A: Neue Aufgabe

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Jonas Brunkow</div>
          <div class="mail-date">10.02.23</div>
        </div>
		<div class="single-mail">
          <input
            type="checkbox"
            
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            
            @click="dialog = true"
          >
            Neue Mitteilung von Vladimir Magalashvili

            <template>
              <div class="new">
                <v-dialog v-model="dialog" persistent width="1024">
                  <template v-slot:activator="{ props }"> </template>
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
                                  von <strong>Nicola Winter</strong> Freitag,
                                  24. Februar 2023, 14:53 PM
                                </p>
                                <p class="normal">
                                  Liebe Studierende der Informatik,
                                </p>
                                <p class="normal">
                                  im Moodle steht das 4. Übungsblatt für Sie
                                  bereit.
                                </p>
                                <p class="normal">
                                  Viel Spaß beim Lösen der Aufgaben!
                                </p>
                                <p class="normal">
                                  Den Artikel zum Algorithmus der Woche für das
                                  Max Flow Problem finden Sie unter folgendem
                                  Link:
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
          </div>

          <div class="mail-consignor">Vladimir Magalashvili</div>
          <div class="mail-date">10.02.23</div>
        </div>

		
        <div class="single-mail">
          <input
            type="checkbox"
            
            id="2"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            onclick="window.location='./test.vue';"
          >
            Übung Datenanalyse
          </div>
          <div class="mail-consignor">Rainer Höhne</div>
          <div class="mail-date">06.02.23</div>
        </div>
        <div class="single-mail">
          <input
            type="checkbox"
            
            id="3"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            onclick="window.location='./test.vue';"
          >
            1. Tag der Informatik am "Pi Tag"
          </div>
          <div class="mail-consignor">Monett Diaz, Dagmar</div>
          <div class="mail-date">06.02.23</div>
        </div>
        <div class="single-mail">
          <input
            type="checkbox"
            
            id="4"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            onclick="window.location='./test.vue';"
          >
            [studierende-gesamt] End of Semester Party - HWR
          </div>
          <div class="mail-consignor">Uniparty Veranstalter</div>
          <div class="mail-date">03.02.23</div>
        </div>
        <div class="single-mail">
          <input
            type="checkbox"
            
            id="1"
            class="checkbox-custom mail-checker"
          />
          <div
            class="mail-subject"
            style="cursor: pointer;"
            onclick="window.location='./test.vue';"
          >
            Übungsblatt2
          </div>
          <div class="mail-consignor">Nicola Winter</div>
          <div class="mail-date">01.02.23</div>
        </div>
      </div>
    </div>
    <div class="right-mail-content">
      <div
        
        density="compact"
        variant="solo"
        label="Search templates"
        append-inner-icon="mdi-magnify"
        single-line
        hide-details
        @click:append-inner="onClick"
      >
        <input
          alt="Mail suchen"
          onfocus="this.value=''"
          value="Mail suchen"
          type="text"
          id="mail-search"
          name="mail-search"
        />
        <div class="main-directories">
          <a href="/">
            <h2>Posteingang:</h2>
          </a>
          <ul>
            <li>
              <a href="/">Entwurf</a>
            </li>
            <li>
              <a href="/">Gesendet</a>
            </li>
            <li>
              <a href="/">Archiv</a>
            </li>
            <li>
              <a href="/">Spam</a>
            </li>
            <li>
              <a href="/">Papierkorb</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="additional-directories">
        <h2>Ordner:</h2>
        <ul>
          <li>
            <a href="./Paetzoldt">Pätzoldt</a>
          </li>
          <li>
            <a href="/">1. Semester</a>
          </li>
          <li>
            <a href="/">2. Semester</a>
          </li>
          <li>
            <a href="/">3. Semester</a>
          </li>
          <li>
            <a href="/">4. Semester</a>
          </li>
          <li>
            <a href="/">5. Semester</a>
          </li>
          <li>
            <a href="/">6. Semester</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import MailToolbar from "~/components/MailToolbar.vue";
import ScheduleList from "~/components/ScheduleList.vue";

const layout = "mail";

export default {
  data: () => ({
    dialog: false
  }),
  loaded: false,
  loading: false,
  
            items: [
                {
                    
                    title: "Pätzoldt",
                    to: "/Paetzoldt"
                }
            ],
        
  components: {
    MailToolbar,
    ScheduleList
  },
  layout: "mail",
  name: "MailPage",
  methods: {
    onClick() {
      this.loading = true;
      setTimeout(() => {
        this.loading = false;
        this.loaded = true;
      }, 2000);
    }
  }
};
</script>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark .head {
  background-color: $color-dark-mode;
}

.theme--dark .mail-subject,
.theme--dark .mail-subject,
.theme--dark .mail-consignor,
.theme--dark .mail-date {
  color: $color-dark-mode;
}

.theme--dark #mail-search a,
.theme--dark .main-directories,
.theme--dark .main-directories a,
.theme--dark .additional-directories,
.theme--dark .additional-directories a {
  color: $color-white;
  text-decoration: none;
}

/* Light Theme Styling */
.theme--light .mail-subject,
.theme--light .mail-subject,
.theme--light .mail-consignor,
.theme--light .mail-date {
  color: $color-dark-mode;
}

.theme--light #mail-search a,
.theme--light .main-directories,
.theme--light .main-directories a,
.theme--light .additional-directories,
.theme--light .additional-directories a {
  color: $color-white;
  text-decoration: none;
}

/* General Mobile Styling */

/* General Desktop Styling */
.main-mail-content {
  display: flex;
  flex-direction: row;
}

.left-mail-content {
  display: flex;
  flex-direction: column;
  width: 80vw;
}

.head {
  display: flex;
  flex-direction: row;
  height: 10vh;
  width: 80vw;
  padding: 1rem;
  border-bottom: 2px solid $color-hwr-red;
}

.mails {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.single-mail {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 3rem;
  border-bottom: 1px solid $color-white;
  background-color: $color-grey-mail;
}

.mail-checker {
  width: 5%;
  margin-left: 2rem;
}

.mail-subject,
.mail-subject1 {
  width: 40%;
}

.mail-consignor {
  width: 45%;
}

.mail-date {
  width: 10%;
}

.mail-subject,
.mail-subject1,
.mail-consignor,
.mail-date {
  padding-left: 0.5rem;
}

.mail-subject1 {
  font-weight: bold;
}

.page-title {
  padding-left: 2rem;
  align-self: center;
  width: 15vw;
}

.right-mail-content {
  display: flex;
  flex-direction: column;
  padding: 1.5rem;
  height: 100vh;
  width: 100vw;
  background-color: $color-hwr-red;
}

#mail-search a,
.main-directories,
.main-directories a,
.additional-directories,
.additional-directories a {
  color: $color-white;
  text-decoration: none;
}

#mail-search {
  background-color: $color-white;
}

.main-directories,
.additional-directories {
  margin: 1rem 0;
}

.main-directories li,
.additional-directories li {
  margin-top: 0.5rem;
  margin-bottom: 1.5rem;
}

.v-btn {
  border: 1px solid $color-hwr-red;
}
</style>
