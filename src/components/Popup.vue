<template>
    <v-dialog max-width="600px">
        <template v-slot:activator="{ on, attrs }">
        <v-btn
          dark
          text
          class="success"
          v-bind="attrs"
          v-on="on"
        >
          Add new Project
        </v-btn>
        
      </template>
        <v-card>
            <v-card-title>
                <h2>Add a new Project</h2>
            </v-card-title>
            <v-card-text>
                <v-form class="px-3" ref="form">
                    <v-text-field label="Title" v-model="title" prepend-icon="folder" :rules="inputRules"></v-text-field>
                    <v-textarea label="Content" v-model="content" prepend-icon="edit" :rules="inputRules"></v-textarea>
                    <v-menu>
                        <template v-slot:activator="{ on, attrs }">
                            <v-text-field
                            prepend-icon="date_range"
                            :value="formattedDate"
                            v-bind="attrs"
                            v-on="on"
                            @click:clear="due = null"
                            :rules="inputRules"
                            ></v-text-field>
                        </template>
                        <v-date-picker
                            v-model="due"
                        ></v-date-picker>
                    </v-menu>
                    <v-btn text class="success mx-0 mt-3" @click="submit">Add project</v-btn>
                </v-form>
            </v-card-text>
        </v-card>
    </v-dialog>
</template>

<script>
import format from 'date-fns/format'
import parseISO from 'date-fns/parseISO'
export default {
    data(){
        return{
            title:'',
            content:'',
            due:null,
            inputRules: [
                v => !!v || 'This field is required',
                v => v.length >= 3 || 'Minimum length is 3 characters'
            ]

        }
    },
    methods:{
        submit(){
            if(this.$refs.form.validate()) {
                console.log(this.title, this.content)
            }     
        }
    },
    computed: {
        formattedDate(){
            return this.due ? format(parseISO(this.due), 'do MMM yyyy') : ''
        },
    }
}
</script>