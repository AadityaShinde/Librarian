<template>
    <v-app-bar app>
        <div class="d-flex align-center" @click="$router.push('/')">
            <v-img alt="Logo" class="mr-2" contain src="../assets/logo.jpg" transition="scale-transition" width="40" />
            {{$const.APP_NAME}}
        </div>
        <v-spacer></v-spacer>
        <v-btn text to="/">Login</v-btn>
        <v-btn text>
            <v-icon>mdi-account-circle</v-icon>
        </v-btn>
    </v-app-bar>
    </template>
    
    <script>
    export default {
    
    }
    </script>
    
    <style lang="scss" scoped>
    
    </style>