<!--template-->
<template>
    <div>
        <!--app bar-->
        <v-app-bar
            dark
            flat
            color="#e4e3e3">
            <v-toolbar-title id="toolbar">Week Days</v-toolbar-title>
                <v-spacer></v-spacer>

            <div class="text-center">

                <v-btn color="pink" icon @click="remove">
                    <v-icon>mdi-minus-box</v-icon>
                </v-btn>

            </div>
        </v-app-bar>
        <!--end app bar-->
        
        <v-container>
            <v-row dense>
                
                <!--col-->
                <v-col 
                cols="12">

                    <v-chip
                        @click="addSaturday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-1-box-multiple-outline</v-icon>
                            Saturday
                    </v-chip>

                    <v-chip
                        @click="addSunday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-2-box-multiple-outline</v-icon>
                            Sunday
                    </v-chip>

                    <v-chip
                        @click="addMonday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-3-box-multiple-outline</v-icon>
                            Monday
                    </v-chip>

                    <v-chip
                        @click="addTuesday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-4-box-multiple-outline</v-icon>
                            Tuesday
                    </v-chip>

                    <v-chip
                        @click="addWednesday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-5-box-multiple-outline</v-icon>
                            Wednesday
                    </v-chip>

                    <v-chip
                        @click="addThursday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-6-box-multiple-outline</v-icon>
                            Thursday
                    </v-chip>

                    <v-chip
                        @click="addFriday"
                        class="ma-2"
                        color="pink"
                        label
                        text-color="white"
                    >
                        <v-icon left>mdi-numeric-7-box-multiple-outline</v-icon>
                            Friday
                    </v-chip>
                    
                </v-col>
                <!--end col-->

                <!--col-->
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
                <!--end col-->

                <!--col-->
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
                <!--end col-->
            </v-row>
        </v-container>
    </div>
</template>
<!--end template-->

<!--script-->
<script>
    export default {
        methods: {
            addSaturday () {
                this.items.push( {
            color: '#fbd46d',
            name: 'Saturday',
            weekend: 'weekend : yes',
        })
            }, 
            addSunday () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Sunday',
            weekend: 'weekend : no',
        })
            },
            addMonday () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Monday',
            weekend: 'weekend : no',
        })
            },
            addTuesday () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Tuesday',
            weekend: 'weekend : no',
        })
            },
            addWednesday () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Wednesday',
            weekend: 'weekend : no',
        })
            },
            addThursday () {
                this.items.push( {
            color: '#84a9ac',
            name: 'Thursday',
            weekend: 'weekend : no',
        })
            },
            addFriday () {
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
<!--end script-->

<!--style-->
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
<!--end style-->