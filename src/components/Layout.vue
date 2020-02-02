<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app >
      <v-list dense>
        <v-list-item v-for="item in items"
                      :key="item.title"
                      :href="item.href"
                      link>
            <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
        </v-list-item>

        <a href="https://buttercms.com"><img src="https://cdn.buttercms.com/JSSDbrHPSnGlLUcyHTn5" style="width: 122px; height:31px; position: absolute; left: 0; bottom: 0;" title="ButterCMS" alt="ButterCMS"></a>

      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="header">Welcome to SohailRahman.net</v-toolbar-title>
    </v-app-bar>

    <AboutMe />
    
  </v-app>
</template>

<script>
import AboutMe from './AboutMe';

export default {
    components: {
      AboutMe
    },
    props: {
      source: String,
    },
    data: () => ({
      drawer: null,
      items: [
                { title: 'Home', icon: 'home', href: "http://SohailRahman.net" },
                { title: 'Blog (Coming Soon!)', icon: 'note', href: "http://Blog.SohailRahman.net" },
                { title: 'GitHub', icon: 'code', href: "https://github.com/Sohail92" },
                { title: 'LinkedIn', icon:'group', href: "https://www.linkedin.com/in/sohailrahman/"},
                { title: 'Contact', icon: 'email', href: `mailto:${'contact@sohailrahman.net'}`}
            ],
    }),
    created () {
      this.$vuetify.theme.dark = true
    },
  }
</script>

<style>
#inspire {
        font-family:Consolas, 'Lucida Console', 'DejaVu Sans Mono', monospace;
}
</style>
