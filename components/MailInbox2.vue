<template>
  <div>
    <v-card class="mx-auto" max-width="100%">
      <v-card-text>
        <p class="textSubject">Übung Datenanalyse</p>
        <p class="textSubject">
          von <strong>Rainer Höhne</strong> Freitag, 24. Februar 2023, 08:38 AM
        </p>
        <p class="normal">Liebe Studentinnen und Studenten,</p>
        <p class="normal">bitte beachten Sie, dass es jetzt natürlich auch zu Bayes / 1R / Entscheidungsbäume ein Übungsblatt in Moodle gibt, dass Sie bitte bearbeiten sollten.</p>
        <p class="normal">
          Viele Grüße, <br />
          Rainer Höhne.    <br />
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
