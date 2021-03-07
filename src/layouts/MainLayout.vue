<template>
  <q-layout view="lHh Lpr lFf">
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

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
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
        <q-item
          clickable
          tag="a"
          :to="{name: 'DataPage'}"
        >
          <q-item-section
            avatar
          >
            <q-icon name="o_add_box" />
          </q-item-section>

          <q-item-section>
            <q-item-label>Add Data</q-item-label>
            <q-item-label caption>
              Json, CSV or excel file
            </q-item-label>
          </q-item-section>
        </q-item>
        <q-item
          clickable
          tag="a"
          :to="{name: 'VizPage'}"
        >
          <q-item-section
            avatar
          >
            <q-icon name="add_chart" />
          </q-item-section>

          <q-item-section>
            <q-item-label>Visualize Data</q-item-label>
            <q-item-label caption>
              Visualize data by line, bar, etc.
            </q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false,
    }
  }
}
</script>
