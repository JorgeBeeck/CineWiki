<template>
  <div>
    <header>
      <div>
        <b-sidebar
          type="is-warning"
          :fullheight="fullheight"
          :fullwidth="fullwidth"
          :overlay="overlay"
          :right="right"
          :open.sync="open"
        >
          <b-button size="is-large" style="border: 0px" type="is-warning" @click="open = false">
            <h1 class="title">X</h1>
          </b-button>

          <div class="p-1">
            <b-menu>
              <b-menu-list label="Menu">
                <b-menu-item icon="information-outline" label="Info"></b-menu-item>
                <b-menu-item icon="settings">
                  <template slot="label" class="has-background-black" slot-scope="props">
                    Administrator
                    <b-icon
                      class="is-pulled-right"
                      :icon="props.expanded ? 'menu-down' : 'menu-up'"
                    ></b-icon>
                  </template>
                  <b-menu-item icon="account" label="Users"></b-menu-item>
                  <b-menu-item icon="cellphone-link">
                    <template slot="label">
                      Devices
                      <b-dropdown
                        aria-role="list"
                        class="is-pulled-right"
                        position="is-bottom-left"
                      >
                        <b-icon icon="dots-vertical" slot="trigger"></b-icon>
                        <b-dropdown-item aria-role="listitem">Action</b-dropdown-item>
                        <b-dropdown-item aria-role="listitem">Another action</b-dropdown-item>
                        <b-dropdown-item aria-role="listitem">Something else</b-dropdown-item>
                      </b-dropdown>
                    </template>
                  </b-menu-item>
                  <b-menu-item icon="cash-multiple" label="Payments" disabled></b-menu-item>
                </b-menu-item>
                <b-menu-item icon="account" label="My Account">
                  <b-menu-item label="Account data"></b-menu-item>
                  <b-menu-item label="Addresses"></b-menu-item>
                </b-menu-item>
              </b-menu-list>
              <b-menu-list>
                <b-menu-item label="Expo" icon="link" tag="router-link" target="_blank" to="/expo"></b-menu-item>
              </b-menu-list>
              <b-menu-list label="Actions">
                <b-menu-item label="Logout"></b-menu-item>
              </b-menu-list>
            </b-menu>
          </div>
        </b-sidebar>

        <b-button size="is-large" style="border: 0px" type="is-warning" @click="open = true">
          <div class="iconmenu"></div>
          <div class="iconmenu"></div>
          <div class="iconmenu"></div>
        </b-button>
      </div>
    </header>
    <br />
    <main>
      <nuxt />
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      open: false,
      overlay: true,
      fullheight: true,
      fullwidth: false,
      right: false
    };
  }
};
</script>

<style>
.iconmenu {
  width: 35px;
  height: 5px;
  background-color: black;
  margin: 6px 0;
}

.p-1 {
  padding: 1em;
}

html {
  background-color: #363636;
  margin: 15px;
}
</style>