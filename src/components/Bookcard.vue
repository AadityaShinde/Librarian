<template>
    <div>
        <v-list-item>
            <v-list-item-avatar rounded="0" size="60">
                <v-img :src="item.img"></v-img>
            </v-list-item-avatar>
            <v-list-item-content @click="$emit('click')">
                <v-list-item-title>{{ item.title }}</v-list-item-title>
                <v-list-item-subtitle class="caption">{{ item.author.name }}</v-list-item-subtitle>
                <v-list-item-subtitle>{{ item.pages }} pages</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
                <v-menu bottom left>
                    <template v-slot:activator="{ on, attrs }">
                        <v-btn icon v-bind="attrs" v-on="on">
                            <v-icon>mdi-dots-vertical</v-icon>
                        </v-btn>
                    </template>
                    <v-list>
                        <v-list-item @click="$router.push('/books/' + item._id)">
                            <v-list-item-title>Edit</v-list-item-title>
                        </v-list-item>
                        <v-list-item @click="$emit('delete')">
                            <v-list-item-title>Delete</v-list-item-title>
                        </v-list-item>
                        <v-list-item @click="$emit('')">
                            <v-list-item-title>Issue</v-list-item-title>
                        </v-list-item>
                        <v-list-item @click="$emit('')">
                            <v-list-item-title>Return</v-list-item-title>
                        </v-list-item>
                    </v-list>
                </v-menu>
                <v-chip icon label>Status</v-chip>
            </v-list-item-action>
        </v-list-item>
        <v-divider></v-divider>
    </div>
</template>
    
<script>
export default {
    props: {
        item: {
            type: Object,
            required: true
        }
    },
}
</script>
    
<style lang="scss" scoped></style>