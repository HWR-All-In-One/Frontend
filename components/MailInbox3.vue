<template>
  <div>
    <v-card class="mx-auto" max-width="100%">
      <v-card-text>
        <p class="textSubject">Notenübersichten 3. Semester - IT2021</p>

        <p class="textSubject">
          von <strong>Jeanette Pätzoldt</strong> Freitag, 1. Februar 2023, 10:48
          AM
        </p>

        <p class="textSubject">
          CC: Monett Diaz, Dagmar
        </p>

        <p class="normal">Liebe Studierende des Informatik-Jahrgangs 2021,</p>

        <p class="normal">
          wir haben Ihnen soeben Ihre letzten Prüfungsergebnisse aus dem 3.
          Semester via E-Mail mitgeteilt. Dieser E-Mail sind auch Ihre
          Notenübersichten beigefügt, die Sie bitte entsprechend an Ihre
          Ausbildungsunternehmen weiterleiten.
        </p>

        <p class="normal">
          Ihre Ausbildungsunternehmen erhalten diese E-Mail in Kopie zur
          Kenntnis.
        </p>

        <p class="normal">
          Herzliche Grüße <br />

          J. Pätzoldt <br />

          --------------------------------------------------------------------<br />
          Studiengangsbüro Informatik <br />
          Tel.: +49 (0)30 30877-2121 <br />
          Hochschule für Wirtschaft und Recht Berlin<br />
          Fachbereich Duales Studium <br />
          Wirtschaft • Technik <br />
          Haus 5, Raum 5.3021 <br />
          Alt-Friedrichsfelde 60 <br />
          D-10315 Berlin <br />
          <a href="www.hwr-berlin.de">www.hwr-berlin.de</a>
        </p>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    reveal: false
  })
};
</script>

<style>
p.textSubject {
  text-align: left;
  font-weight: bold;
}

p.thick {
  font-weight: bold;
  text-align: left;
}

p.normal {
  font-weight: normal;
  text-align: left;
}
</style>
