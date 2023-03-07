<template>
  <div>
    <v-card class="mx-auto" max-width="100%">
      <v-card-text>
        <p class="textSubject">21004262 IT1151 FS 4 TIT21A: 4. Übungsblatt</p>
        <p class="textSubject">
          von <strong>Nicola Winter</strong> Freitag, 24. Februar 2023, 14:53 PM
        </p>
        <p class="normal">Liebe Studierende der Informatik,</p>
        <p class="normal">im Moodle steht das 4. Übungsblatt für Sie bereit.</p>
        <p class="normal">Viel Spaß beim Lösen der Aufgaben!</p>
        <p class="normal">
          Den Artikel zum Algorithmus der Woche für das Max Flow Problem finden
          Sie unter folgendem Link:
          <a href="https://algo.rwth-aachen.de/~algorithmus/algo23.php"
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
