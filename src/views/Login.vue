<template>
    <div class="center">  
        <v-row>
            <v-col cols="10" offset="1">
                <v-avatar color="primary" size="95" tile>
                    <v-img src="@/assets/logo.jpg"></v-img>

                </v-avatar>
                <v-text-field label="username" v-model="username" outlined></v-text-field>
                <v-text-field label="Password" v-model="Password" type="password" outlined></v-text-field>
                <v-btn color="secondary" elevation="2" @click="authenticate()">Login</v-btn>
            </v-col>
        </v-row>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                username: "", 
                password: ""
            }
            
        },
        methods: {

        }
        
    }
</script>

<style lang="scss" scoped>

</style>