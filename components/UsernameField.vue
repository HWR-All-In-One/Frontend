<template>
  <div class="container">
    <div class="text-box">
      <h1> HWR AIO </h1>
      <h2> Anmeldung </h2>
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
</template>

<style>

.text-box{
  
}

.LoginButton{
  text-align: center;
  align-self: center;
  height: 20%;
  width: 20%
}

.container{
  display:flex; 
  justify-content: space-evenly;
  flex-flow: column wrap;
  text-align: center;
  margin-top: 15%;
  
}


.userbar{
  text-align: center;
  align-self: center;
  padding: 5%;
  height: 20%;
  width: 40%
}
</style>