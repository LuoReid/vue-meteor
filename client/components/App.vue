<template>
  <div id="#app">
    <h1>Meteor</h1>
    <nav>
      <router-link v-bind:to="{name:'dashboard'}" exact>Dashboard</router-link>
      <router-link v-bind:to="{name:'generate'}">Measure</router-link>
    </nav>
    <router-view />
  </div>
</template>
<style lang="stylus" src="../style.styl" />