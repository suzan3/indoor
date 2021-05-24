<template>
<q-layout view="lHh Lpr lFf">
    <q-header elevated>
        <q-toolbar class="q-px-xl q-mt-sm">
            <!-- <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        /> -->

            <!-- <q-toolbar-title> -->
            <img src="~assets/logo.png" class="q-ma-sm q-mr-xl logo" width="55px" alt="">
            <!-- </q-toolbar-title> -->
            <div class="nav-link">
                Solutions
            </div>
            <div class="nav-link">
                Resources
            </div>
            <div class="nav-link">
                Products
            </div>
            <q-space />
            <div class="search">
                <img src="~assets/search.png" width="25px" alt="">
            </div>
        </q-toolbar>
    </q-header>

    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
        <router-view />
    </q-page-container>
</q-layout>
</template>

<style lang="scss">
.q-header{
    position: absolute !important;
}

@media only screen and (max-width: 775px) {
    .q-toolbar {
        padding-left: 4px !important;
        padding-right: 4px !important;

        .logo {
            margin-right: 0 !important;
            width: 35px;
        }
    }
}

.q-layout__section--marginal {
    background-color: transparent !important;
}

.q-toolbar {
    position: absolute !important;
}

.search {
    cursor: pointer;
}

.nav-link {
    font-family: 'Roboto-Bold';
    font-size: 15px;
    margin-left: 6px;
    margin-right: 6px;
}
</style>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [{
        title: 'Docs',
        caption: 'quasar.dev',
        icon: 'school',
        link: 'https://quasar.dev'
    },
    {
        title: 'Github',
        caption: 'github.com/quasarframework',
        icon: 'code',
        link: 'https://github.com/quasarframework'
    },
    {
        title: 'Discord Chat Channel',
        caption: 'chat.quasar.dev',
        icon: 'chat',
        link: 'https://chat.quasar.dev'
    },
    {
        title: 'Forum',
        caption: 'forum.quasar.dev',
        icon: 'record_voice_over',
        link: 'https://forum.quasar.dev'
    },
    {
        title: 'Twitter',
        caption: '@quasarframework',
        icon: 'rss_feed',
        link: 'https://twitter.quasar.dev'
    },
    {
        title: 'Facebook',
        caption: '@QuasarFramework',
        icon: 'public',
        link: 'https://facebook.quasar.dev'
    },
    {
        title: 'Quasar Awesome',
        caption: 'Community Quasar projects',
        icon: 'favorite',
        link: 'https://awesome.quasar.dev'
    }
];

export default {
    name: 'MainLayout',
    components: {
        // EssentialLink
    },
    data() {
        return {
            leftDrawerOpen: false,
            essentialLinks: linksData
        }
    }
}
</script>
