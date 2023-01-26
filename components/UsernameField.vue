<template>
  <div class="container">
    <div class="box">
      <div class="text-box">
        <h1> Anmeldung </h1>
        <h3> Weiter zum Userspace </h3>
      </div>
      <div class="userbar">
              <v-text-field
                hide-details
                single-line
                filled
                outlined
                label = "Benutzer"
                hint ="Dein Nutzername von Moodle"
              >
            </v-text-field>
      </div>
      <div class="LoginButton" >
        <div id="inspire">
          <v-btn block class="button">
            Continue
          </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>

<style>

.LoginButton{
  text-align: center;
  height: 20%;
  width: 80%;
}

.container{
  display:flex; 
  justify-content: space-evenly;
  flex-flow: column wrap;
  text-align: center;
  margin-top: 5%;
  font: 1em helvetica;
  height: 50%;


}

.box{
  display:flex; 
  justify-content: space-evenly;
  flex-flow: column wrap;
  text-align: center;
  align-self: center;
  width: 20%;
  height: 100%;
  border-style: solid;
}

.userbar{
  text-align: center;
  padding-top: 1%;
  padding-bottom: 5%;
  height: 20%;
  width: 80%
}

.text-box{
  line-height: 2;
}


</style>