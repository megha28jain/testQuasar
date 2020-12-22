<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <div class="q-pa-md q-gutter-sm">
        <q-btn color="deep-orange" glossy label="Logo" />
      </div>
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          PROJECT DETAILS
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          INVESTMENT
        </q-item-label>
        <EssentialLink
          v-for="link in investLinksData"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Overview',
    icon: '',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Documents',
    icon: '',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'FAQ & Contact',
    icon: '',
    link: '/'
  }
  // {
  //   title: 'Forum',
  //   caption: 'forum.quasar.dev',
  //   icon: 'record_voice_over',
  //   link: 'https://forum.quasar.dev'
  // },
  // {
  //   title: 'Twitter',
  //   caption: '@quasarframework',
  //   icon: 'rss_feed',
  //   link: 'https://twitter.quasar.dev'
  // },
  // {
  //   title: 'Facebook',
  //   caption: '@QuasarFramework',
  //   icon: 'public',
  //   link: 'https://facebook.quasar.dev'
  // },
  // {
  //   title: 'Quasar Awesome',
  //   caption: 'Community Quasar projects',
  //   icon: 'favorite',
  //   link: 'https://awesome.quasar.dev'
  // }
]

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData,
      investLinksData: [
        {
          title: 'Invitation & NDA',
          icon: '',
          link: 'https://github.com/quasarframework'
        },
        {
          title: 'Terms & Commitment',
          icon: '',
          link: 'https://github.com/quasarframework'
        }
      ]
    }
  }
}
</script>
