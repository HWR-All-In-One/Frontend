<template>
  <div>
    <v-alert text color="info">
      <h3 class="text-h5">
        Inormation
      </h3>
      <div>
        Wenn Sie noch weitere Informationen benötigen, melden sie sich bitte bei
        uns.
      </div>

      <v-divider class="my-4 info" style="opacity: 0.22"></v-divider>

      <v-row align="center" no-gutters>
        <v-col class="grow"> </v-col>
        <v-col class="shrink">
          <v-btn color="info" outlined>
            Kontakt
          </v-btn>
        </v-col>
      </v-row>
    </v-alert>

    <v-alert text dense color="teal" icon="mdi-clock-fast" border="left">
      erfolgreich angemeldet. Bitte warten Sie einen Moment.
    </v-alert>
    <v-alert text prominent type="error" icon="mdi-cloud-alert">
      Verbindung fehlgeschlagen. Bitte überprüfen sie ihre Netzwerkverbindung.
    </v-alert>
  </div>
</template>
