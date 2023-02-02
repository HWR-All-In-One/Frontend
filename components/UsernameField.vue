<template>
    <div class="box">
      <div class="text-box">
        <h1 style="color:red"> HWR Student Portal </h1>
        <img src="~/assets/baer.jpeg" height="50%" >
        <h2> Anmeldung </h2>
        <h3> Weiter zum Userspace </h3>
      </div>
      <div class="userbar">
              <v-text-field
                hide-details
                single-linenpm
                filled
                outlined
                label = "Benutzer"
                hint ="Dein Nutzername von Moodle"
              >
            </v-text-field>
      </div>
      <a href="#">Forgot your password?</a>
        <v-btn class="buttonCreate">button</v-btn>


        <v-btn class="buttonContinue">
          Continue
        </v-btn>
    </div>
</template>

<style>

a{
  align-self: flex-start;
  margin-left: 11%;

}

.reihe{
  position: relative;
  
}

.buttonCreate{
  position: relative;
  text-align: center;
  align-self: center;
  width: 80%;
}

.buttonContinue{
  line-height: 1.25;
  background: #FC6E51;
  text-decoration: none;
  color: white;
  font-size: 16px;
  letter-spacing: .08em;
  text-transform: uppercase;
  position: relative;
  transition: background-color .6s ease;
  overflow: hidden;
  width:80%;
  align-self: center;
  margin-bottom: 1%;
}
  


.box{
  position: fixed;
  display:flex; 
  justify-content: space-evenly;
  flex-flow: column wrap;
  text-align: center;
  align-self: center;
  width: 25%;
  height: 65%;
  border-style: solid;
  border-radius: 2ch;
  border-color: #D50B2E;
}

.userbar{
  text-align: center;
  align-self: center;
  height: 10%;
  width: 80%
}

.text-box{
  line-height: 2;
}



</style>