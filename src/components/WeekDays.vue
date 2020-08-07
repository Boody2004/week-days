<template>
    <div>
        <v-app-bar
            dark
            flat
            color="#e4e3e3">
            <v-toolbar-title id="toolbar">Week Days</v-toolbar-title>
                <v-spacer></v-spacer>
                
<!--////////////////////////////////////icon///////////////////////////////////////////-->

            <div class="text-center">

                <v-btn icon @click="ad">
                    <v-icon>mdi-numeric-1-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="add">
                    <v-icon>mdi-numeric-2-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="addd">
                    <v-icon>mdi-numeric-3-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="adddd">
                    <v-icon>mdi-numeric-4-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="addddd">
                    <v-icon>mdi-numeric-5-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="adddddd">
                    <v-icon>mdi-numeric-6-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="addddddd">
                    <v-icon>mdi-numeric-7-box-multiple-outline</v-icon>
                </v-btn> 

                <v-btn icon @click="remove">
                    <v-icon>mdi-minus-box</v-icon>
                </v-btn>

            </div>

        </v-app-bar>
        <v-container>
            <v-row dense>

<!--////////////////////////////////////v-col///////////////////////////////////////////-->

                <v-col
                cols="12"
                flat>
                    <v-card
                        color="#385F73"
                        dark>
                        <v-card-title class="headline">Find Out Today And Weekends</v-card-title>
                        <v-card-subtitle>
                            A gift for the older brother and virtuous teacher Hazem .
                        </v-card-subtitle>
                        <v-card-actions></v-card-actions>
                    </v-card>
                </v-col>

<!--////////////////////////////////////v-col///////////////////////////////////////////-->

                <v-col
                    v-for="(item, i) in items"
                    :key="i"
                    cols="12"
                    flat>
                    <v-card
                        :color="item.color"
                        dark>
                        <div class="d-flex flex-no-wrap justify-space-between">
                            <div>
                                <v-card-title 
                                    class="headline"
                                    v-text="item.name">
                                </v-card-title>
                                <v-card-subtitle v-text="item.weekend" id="subtitle"></v-card-subtitle>
                            </div>
                        </div>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>
<!--////////////////////////////////////Script///////////////////////////////////////////-->
<script>
    export default {
        methods: {
            ad () {
                this.items.push( {
            color: '#fbd46d',
            name: 'Saturday',
            weekend: 'weekend : yes',
        })
            }, 
            add () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Sunday',
            weekend: 'weekend : no',
        })
            },
            addd () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Monday',
            weekend: 'weekend : no',
        })
            },
            adddd () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Tuesday',
            weekend: 'weekend : no',
        })
            },
            addddd () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Wednesday',
            weekend: 'weekend : no',
        })
            },
            adddddd () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Thursday',
            weekend: 'weekend : no',
        })
            },
            addddddd () {
                this.items.push( {
            color: '#fbd46d',
            name: 'Friday',
            weekend: 'weekend : yes',
        })
            },
            remove () {
                if (this.items.length > 7) {
                    this.items.splice(-1,1)
                }
            }
        },
    data: () => ({
        items: [
        {
            color: '#fbd46d',
            name: 'Saturday',
            weekend: 'weekend : yes',
        },
        {
            color: '#84a9ac',
            name: 'Sunday',
            weekend: 'weekend : no',
        },
        {
            color: '#84a9ac',
            name: 'Monday',
            weekend: 'weekend : no',
        },
        {
            color: '#84a9ac',
            name: 'Tuesday',
            weekend: 'weekend : no',
        },
        {
            color: '#84a9ac',
            name: 'Wednesday',
            weekend: 'weekend : no',
        },
        {
            color: '#84a9ac',
            name: 'Thursday',
            weekend: 'weekend : no',
        },
        {
            color: '#fbd46d',
            name: 'Friday',
            weekend: 'weekend : yes',
        },
        ],
    }),
    }
</script>
<!--////////////////////////////////////Style///////////////////////////////////////////-->
<style>
    #toolbar{
        font-size: 35px;
    }
    #subtitle{
        font-size: 20px;
    }
    #name{
        color: black;
        text-transform: uppercase;
        background-image: linear-gradient(102deg,#84a9ac, #fbd46d, #385F73);
    }
</style>