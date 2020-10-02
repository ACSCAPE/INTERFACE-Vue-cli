<template>
    <div class="interface">
      <v-row class="Up">
        <div class="ULeft">
          <v-row class="visual">
            <div class="reponse"></div>
            <div class="time"></div>
          </v-row>
        </div>
        <v-row class="URight">
          <div class="tchat">
            <p class="titleTchat">Discussion ()</p>
            <div class="bar"></div>
            <Tchat />
          </div>
          <div class="users">
            <p class="titleTchat">Utilisateurs ()</p>
            <div class="bar"></div>
            <Users />
          </div>
        </v-row>
      </v-row>
      <v-row class="Down">
        <div class="DLeft">
        </div>
        <div class="DRight">
          <p class="titleTchat">Notes partagées</p>
          <div class="bar"></div>
          <TxtShared />
        </div>
      </v-row>
    </div>
</template>

<script>
  import Tchat from './Tchat'
  import Users from './Users'
  import TxtShared from './TxtShared'

  export default{
    name: 'App',
    components: {
      Tchat,
      Users,
      TxtShared
    }
  }
</script>

<style>
  .interface{height: 100%;}
  .Up{height: 74%;}
  .Down{height: 26%;}
  .ULeft{background-color: gray;}
  .visual{width: 100%;height: 100%;}
  .reponse,.time{background-color: rgba(0,0,0,0.5);border-radius: 10px;}
  .reponse{height: 115px;width: 266px;margin-top: 10px;margin-left:10px;}
  .time{height: 61px;width: 161px;float: right;margin-top: 10px;margin-right: 10px;margin-left: auto;}
  .URight,.Up,.Down,.visual{margin: 0!important;}
  .tchat{width: 70%;}
  .titleTchat{text-align: left;margin-left: 25px;margin-bottom:5px!important;font-size:12px;margin-top:5px;height: 18px;overflow: hidden;}
  .bar{background-color: black;height: 1px;width: 40%;margin-left: 25px;}
  .users{background-color: #E2E2E2;width: 30%;}
  .users .bar{width: 70%;}
  .DLeft{background-color: white;}
  .DRight{background-color: #FFE6EB;}
  .ULeft,.DLeft{width: 72%;}
  .URight,.DRight{width: 28%;}
</style>
