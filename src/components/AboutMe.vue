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
                                                    <img src="../../src/assets/cropped.jpg">
                                                </v-avatar>
                                                <v-list-item>
                                                    <v-list-item-content>
                                                        <v-list-item-title class="title">Sohail Rahman</v-list-item-title>
                                                        <v-list-item-subtitle class="hidden-md-and-up">Senior Web Developer - TUI Group</v-list-item-subtitle>
                                                        <v-list-item-subtitle class="hidden-sm-and-down">Senior Web Developer</v-list-item-subtitle>
                                                        <v-list-item-subtitle class="hidden-sm-and-down">TUI Group</v-list-item-subtitle>



                                                    </v-list-item-content>
                                                </v-list-item>
                                            </v-card>
                                        </v-flex>

                                        <!-- Information about me card -->
                                        <v-flex d-flex md9>
                                            <v-card color="steel">
                                                <v-card-text>Hi, I'm an experienced Software Developer with a first class degree in Computer Science from University of Teesside. Currently I work for TUI Group in Stockton-On-Tees as a Senior Web Developer. In the past I have worked for Dupont Teijin Films in Dumfries as a Software Engineer. I am a Microsoft Certified Professional and looking to gain further certification in the near future. Outside of work I enjoy keeping up to date with the latest technological advancements and learning more about the ever-changing software industry.</v-card-text>
                                                <v-card-text>I have experience developing bespoke Desktop/Web Applications and APIs. In addition to this I have a good understanding of database and search technologies such as SQL Server and Apache Solr. My main interests are in software architecture, utilising the latest technologies and writing high quality, maintainable code. </v-card-text>
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
                                <ul>
                                    <li>Most of my experience is with C# as my programming language of choice. I have used C# to develop both Desktop and Web Applications, RESTful and WCF based Services and more. I have also developed with languages such as Java and Delphi.</li>
                                    <li>I have worked with both SQL and NoSQL technologies in the past such as: SQL Server, MongoDB, CosmosDB and Apache Solr.</li>
                                    <li>In regards to source control I am comfortable with both TFS and Git.</li>
                                    <li>Knowledge of various development tools such as Webpack, Babel, Ninject, Moq, Linters, POSTman, Fiddler and more.</li>
                                </ul>
                            <br/>
                            </v-card>
                        </v-flex>

                        <!-- Current Interests card -->
                        <v-flex >
                            <v-card elevation="10" color="blue darken-4">
                                <v-card-title primary class="title">Current Interests</v-card-title>
                                <ul>
                                    <li>Working with JavaScript frameworks for web development (e.g. Angular or Vue) for building user-interfaces and single-page apps.</li>
                                    <li>Using tools such as Google Analytics to track and report on website traffic.</li>
                                    <li>Developing with ES6 JavaScript and tools such as Webpack for module bundling and Babel as a transpiler.</li>
                                    <li>Working with content management systems such as Umbraco, currently I've worked with Wordpress and Kentico. I feel Umbraco could be valuable to gain some experience in since its open-source and written in Microsoft technologies.</li>
                                </ul>
                                <br/>
                            </v-card>
                        </v-flex>
                </v-flex>
                        
                <v-flex xl3>
                    <v-layout>
                        <!-- Side panel card -->
                        <v-flex hidden-lg-and-down>
                            <v-card elevation="24">
                                    <v-img min-height="735px" src="../../src/assets/2.jpg"></v-img>
                            </v-card>
                        </v-flex>
                    </v-layout>
                </v-flex>

            </v-layout>
  </v-container>
</v-content>
</template>

<script>
export default {  
}
</script>

<style>
.myImage{ margin-left:0px;}
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
</style>