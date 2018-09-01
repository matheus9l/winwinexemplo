<template>
  <v-app id='inspire'>
    <v-navigation-drawer fixed v-model="drawer" app>
      <v-list dense>

        <router-link v-bind:to="{name: 'Lista'}" class="side_bar_link">
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>home</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>Listar prêmios</v-list-tile-content>
          </v-list-tile>
        </router-link>

        <router-link v-bind:to="{name: 'Cadastro'}" class="side_bar_link">
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>contact_mail</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>Cadastrar prêmio</v-list-tile-content>
          </v-list-tile>
        </router-link>

        <router-link v-bind:to="{name: 'Edição'}" class="side_bar_link">
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>contact_mail</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>Editar prêmio</v-list-tile-content>
          </v-list-tile>
        </router-link>

        <router-link v-bind:to="{name: 'Categoriass'}" class="side_bar_link">
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>contact_mail</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>Categorias</v-list-tile-content>
          </v-list-tile>
        </router-link>

      </v-list>
    </v-navigation-drawer>

    <v-toolbar color="#3D8BFF" dark fixed app>
      <v-toolbar-side-icon @click.stop="drawer =! drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Home</v-toolbar-title>
    </v-toolbar>

    <v-content>
      <v-container fluid>
        <div id="app">
          <router-view/>
        </div>
      </v-container>
    </v-content>

  </v-app>
</template>

<script>
import './assets/stylesheets/main.css';

export default {
  name: 'App',
};
</script>

<style>

</style>
