<template>
  <q-layout view="hHh lpR fFf">
    <!-- <span class="portal-headborder"></span> -->
    <div class="row">
      <div class="col-xs-9 col-sm-6 col-md-4">
        <a>
          <img src="~assets/my-indonesia-white.png" width="100px" />
          <div class="portal-claim">The Official Website of Indonesia</div>
        </a>
      </div>
      <div class="col-xs-3 col-sm-6 col-md-4" :desktop-nav="true"></div>
      <q-icon name="menu" class="mobile-nav" size="md" style="color: #ffffff" />
    </div>

    <q-input v-model="searchInput" filled type="search" hint="Search">
      <template v-slot:append>
        <q-icon name="search" />
      </template>
    </q-input>

    <q-input v-model="tel" filled type="tel" hint="Telephone number" />

    <q-input v-model="url" filled type="url" hint="URL" />

    <q-input v-model="time" filled type="time" hint="Native time" />

    <q-input v-model="date" filled type="date" hint="Native date" />

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
// import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: "Politics & Administration",
    icon: "account_balance",
    link: "https://quasar.dev",
  },
  {
    title: "Events & Festivals",
    icon: "theater_comedy",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Tourism & Travel",
    icon: "work",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Business & Economy",
    icon: "insights",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Shopping",
    icon: "shopping_cart",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "IndonesiaFinder",
    icon: "manage_search",
    link: "https://facebook.quasar.dev",
  },
];

export default {
  name: "MainLayout",
  // components: { EssentialLink },
  data() {
    return {
      searchInput: "Search something",
      right: false,
      essentialLinks: linksData,
    };
  },
  computed: {
    inputSearch: {
      get() {
        return "hello";
      },
      set(v) {
        this.inputSearch = "hello22";
      },
    },
  },

  methods: {
    onReset() {},
    onSubmit() {},
  },
};
</script>

<style lang="scss">
// app global css in SCSS form
.portal-claim {
  display: inline-block;
  position: relative;
  margin: 1em 0 0 1.2em;
  vertical-align: top;
  color: #ffffff;
  font-size: 0.875rem;
  font-weight: 400;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.portal-headborder {
  height: 0.3125rem;
  width: 100%;
  background-color: #ff0000;
  display: block;
  position: absolute;
  left: 0;
  top: 0;
}
.portal-headborder::after {
  height: 0.3125rem;
  width: 31%;
  background-color: #ffffff;
  display: block;
  content: " ";
  float: right;
}
.row {
  padding: 10px 15px;
  background: #376783;
  border: 1px solid rgba(86, 61, 124, 0.2);
}
.row > div:last-child {
  display: none;
}
.row + .row {
  margin-top: 1rem;
}
.mobile-nav {
  display: none;
}

// MEDIA QUERY
@media (max-width: 720px) {
  .portal-claim {
    display: none;
  }
  .mobile-nav {
    display: inline;
    float: right;
    position: absolute;
    right: 0;
    padding-right: 15px;
  }
}
</style>
