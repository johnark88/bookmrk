<template>
  <div id="app">
    <div id="nav">
      <b-nav fill tabs>
        <b-nav-item active> <router-link to="/">Home</router-link> </b-nav-item>
        <b-nav-item> About </b-nav-item>
        <b-nav-item> Work </b-nav-item>
      </b-nav>
      
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #00171f;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #007ea7;
    &.router-link-exact-active {
      color: #007ea7;
    }
  }
}

</style>
