<template>
<div class="app-header">
    <v-row dense>
        <v-col cols="10">
            <h3>{{title}}</h3>
        </v-col>
        <v-col cols="2" class="text-right">
            <v-btn :title="tooltip" text @click="$emit('add')">
                <v-icon>mdi-plus</v-icon>
            </v-btn>
        </v-col>
        <v-col class="px-5">
            <v-text-field placeholder="Search" append-icon="mdi-magnify" @input="$emit('search', $event)"></v-text-field>
        </v-col>
    </v-row>
    <v-row>
    </v-row>
</div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: ''
        },
        tooltip: {
            type: String,
            default: ''
        }
    },
    data() {
        return {
            search: ''
        }
    },
}
</script>

<style lang="scss" scoped>
.app-header{
    padding: 2%;
}
h3{
    margin-left: 1rem;
}
</style>