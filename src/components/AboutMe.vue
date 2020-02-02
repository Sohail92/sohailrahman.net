<template>
<v-content>
    <v-container grid-list-md>
            <v-layout>
                <v-flex lg12 xl9>
                        <!-- About Me container --> 
                        <v-flex>
                            <v-card elevation="24" color="blue">
                                <v-container>
                                    <v-layout wrap>
                                        <!-- Portrait and Title card -->
                                        <v-flex d-flex md3>
                                            <v-card color="steel" width="100%">
                                                <v-avatar class="myImage" :class="{'myImageXS': $vuetify.breakpoint.xs, 'myImageSmall': $vuetify.breakpoint.sm
                                                , 'myImageMedium': $vuetify.breakpoint.md, 'myImageLarge': $vuetify.breakpoint.lg, 'myImageXtraLarge':$vuetify.breakpoint.xl}">
                                                    <img src="../../src/assets/me.jpg">
                                                </v-avatar>
                                                <v-list-item class="centeredText">
                                                    <v-list-item-content>
                                                        <v-list-item-title class="title">Sohail Rahman</v-list-item-title>
                                                        <v-list-item-subtitle class="hidden-md-and-up">Senior Web Developer - CarbonDMP</v-list-item-subtitle>
                                                        <v-list-item-subtitle class="hidden-sm-and-down">Senior Web Developer</v-list-item-subtitle>
                                                        <v-list-item-subtitle class="hidden-sm-and-down">Carbon by Clicksco</v-list-item-subtitle>
                                                    </v-list-item-content>
                                                </v-list-item>
                                            </v-card>
                                        </v-flex>

                                        <!-- Information about me card -->
                                        <v-flex d-flex md9>
                                            <v-card color="steel">
                                                <div v-html="aboutSohail.data.body"></div>
                                                <v-card-actions>
                                                    <v-btn  :href="`mailto:${'contact@sohailrahman.net'}`" color="blue" >                                      
                                                        <v-icon left>mail</v-icon>  Send me an e-mail
                                                    </v-btn>
                                                </v-card-actions>
                                            </v-card>
                                        </v-flex>
                                    </v-layout>
                                </v-container>                           
                            </v-card>
                        </v-flex>

                        <!-- Technologies card -->
                        <v-flex >
                            <v-card elevation="10" color="blue darken-3">
                                <v-card-title primary class="title">Technologies</v-card-title>
                                <div v-html="technologies.data.body"></div>
                            <br/>
                            </v-card>
                        </v-flex>

                        <!-- Current Interests card -->
                        <v-flex >
                            <v-card elevation="10" color="blue darken-4">
                                <v-card-title primary class="title">Current Interests</v-card-title>
                                <div v-html="interests.data.body"></div>
                                <br/>
                            </v-card>
                        </v-flex>
                </v-flex>
                        
                <v-flex xl3>
                    <v-layout>
                        <!-- Side panel card -->
                        <v-flex hidden-lg-and-down>
                            <v-card elevation="24">
                                    <v-img min-height="690" src="../../src/assets/2.jpg"></v-img>
                            </v-card>
                        </v-flex>
                    </v-layout>
                </v-flex>

            </v-layout>
  </v-container>
</v-content>
</template>

<script>
import Butter from 'buttercms';
export const butter = Butter('f8c25828916fe2efad14da59fb81f27af5b58c79');

export default {  
    name: "MyComponent",
    data() {
        return {
            aboutSohail:'',
            technologies:'',
            interests:''
        };
    },
    methods: {
        getAboutSohail() {
            butter.post.retrieve('aboutsohail')
                .then((res) => {
                    console.log(res.data)
                    this.aboutSohail = res.data
                }).catch((res) => {
                    console.log(res)
                })
            },
        getTechnologies() {
            butter.post.retrieve('technologies')
                .then((res) => {
                    console.log(res.data)
                    this.technologies = res.data
                }).catch((res) => {
                    console.log(res)
                })
            },
            getInterests() {
            butter.post.retrieve('interests')
                .then((res) => {
                    console.log(res.data)
                    this.interests = res.data
                }).catch((res) => {
                    console.log(res)
                })
            }
    },
    created() {
        this.getAboutSohail(),
        this.getTechnologies(),
        this.getInterests()
    }
}
</script>

<style>
.myImage{ margin-left:0px; display: block !important; margin:0 auto; border-top-left-radius: 0 !important; border-top-right-radius: 0 !important;}
.myImageXS {
    height:75px !important;
    width:75px !important;
}
.myImageSmall {
    height:100px !important;
    width:100px !important;
}
.myImageMedium {
    height:140px !important;
    width:140px !important;
}
.myImageLarge {
    height:170px !important;
    width:170px !important;
}
.myImageXtraLarge {
    height:200px !important;
    width:200px !important;
} 
li{
    margin-left:20px !important;
    margin-right:20px !important;
}
ul {
  list-style-type: square !important;
}
.centeredText{
    text-align: center;
}
</style>