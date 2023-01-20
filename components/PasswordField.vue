<template>
  <div class="flex-box">
    <div class="userbar">
            <v-text-field
              hide-details
              single-line
              filled
              outlined
              label = "Passwort"
              hint ="Dein Passwort von Moodle"
            ></v-text-field>
    </div>
  </div>
  </template>

<style>

.flex-box {
	display:flex; 
	justify-content: space-around;
}

.userbar{
  text-align: center;
  align-self: center;
  height: 20%;
  width: 20%
}
</style>