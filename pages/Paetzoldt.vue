<template>
  <div class="main-mail-content">
    <div class="left-mail-content">
      <div class="head">
        <h1 class="page-title">Pätzoldt</h1>
        <MailToolbar1 />
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
            Notenübersichten 3. Semester - IT2021

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
          <div class="mail-date">27.0.23</div>
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
            Notenbekanntgabe 3. Semester

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
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
            AW: PTB3 Bewertung

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
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
            PTB3 Bewertung

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
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
            21004001 IT2321 FS 3 TIT21A: Einsicht PTB Bewertung

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
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
            Notenbekanntgabe 3. Semester

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
          <div class="mail-date">05.01.23</div>
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
            GitHub-Konten / Modul Studienprojekt I, 4.Sem., IT21

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
          <div class="mail-date">20.12.22</div>
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
            Vorlesungsausfall Webprogrammierung

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
          <div class="mail-date">18.12.22</div>
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
            Notenübersichten 2. Semester - IT2021

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
                                  von <strong>Pätzoldt, Jeanette</strong> Freitag,
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
                                  Prof. Dr. Pätzoldt, Jeanette <br />
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

          <div class="mail-consignor">Pätzoldt, Jeanette</div>
          <div class="mail-date">14.12.22</div>
        </div>


		



		

		
        
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
