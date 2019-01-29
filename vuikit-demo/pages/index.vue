<template>
  <div>
    <vk-navbar transparent>
      <vk-navbar-nav slot="right" class="uk-visible@m">
        <vk-navbar-nav-item title="Home" active></vk-navbar-nav-item>
        <vk-navbar-nav-dropdown title="Parent">
          <vk-navbar-nav-dropdown-nav>
              <vk-nav-item title="Active" active></vk-nav-item>
              <vk-nav-item title="Item"></vk-nav-item>
              <vk-nav-item title="Item"></vk-nav-item>
          </vk-navbar-nav-dropdown-nav>
        </vk-navbar-nav-dropdown>
        <vk-navbar-nav-item title="Item"></vk-navbar-nav-item>
      </vk-navbar-nav>
      <vk-navbar-nav slot="right">
          <vk-navbar-toggle @click="primaryNav = true" class="uk-hidden@m"></vk-navbar-toggle>
      </vk-navbar-nav>
    </vk-navbar>
    <h1 class="uk-heading-hero">Hello World</h1>
    <h2 class="uk-text-lead">A Simple example for Nuxt.js + Vuikit</h2>
    <p class="uk-text-meta">Vuikit is a CSS framework based on Uikit.</p>
    <p></p>
    <vk-card type="primary">
      <vk-card-title>Nuxt + Vuikit</vk-card-title>
      <div class="uk-inline">
        <vk-button>Hover</vk-button>
        <vk-dropdown>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
        </vk-dropdown>
      </div>
      <div class="uk-inline">
        <vk-button>Click</vk-button>
        <vk-dropdown mode="click">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
        </vk-dropdown>
        <vk-button @click="show = true">Open</vk-button>
        <vk-modal :show.sync="show">
          <vk-modal-close @click="show = false"></vk-modal-close>
          <vk-modal-title slot="header">Modal Title</vk-modal-title>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          <div slot="footer" class="uk-text-right">
            <vk-button class="uk-margin-small-right" @click="show = false">Cancel</vk-button>
            <vk-button type="primary">Save</vk-button>
          </div>
        </vk-modal>
      </div>
      <hr class="uk-divider-icon">
      <vk-icon icon="heart" />
    </vk-card>

    <vk-offcanvas-content>
      <vk-offcanvas overlay :show.sync="primaryNav">
        <vk-offcanvas-close @click="primaryNav = false"></vk-offcanvas-close>
        <vk-offcanvas-bar class="uk-flex uk-flex-column">
          <vk-nav type="primary" center class="uk-margin-auto-vertical">
            <vk-nav-item title="Active" active></vk-nav-item>
            <vk-nav-item-parent title="Parent">
              <vk-nav-item title="Sub Item"></vk-nav-item>
              <vk-nav-item title="Sub Item"></vk-nav-item>
            </vk-nav-item-parent>
            <vk-nav-item-header title="Header"></vk-nav-item-header>
            <vk-nav-item title="Item" icon="table"></vk-nav-item>
            <vk-nav-item title="Item" icon="thumbnails"></vk-nav-item>
            <vk-nav-item-divider></vk-nav-item-divider>
            <vk-nav-item title="Item" icon="trash"></vk-nav-item>
          </vk-nav>
        </vk-offcanvas-bar>
      </vk-offcanvas>
    </vk-offcanvas-content>
  </div>
</template>

<script>
export default {
  data() {
    return {
      primaryNav: false,
      show: false,
    }
  }
}
</script>
