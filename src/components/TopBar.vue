<template>
  <nav class="top-bar" :class="{open: open}">
      <div class="wrapper">
        <router-link to="/" class="brand">
            Resilence
        </router-link>
        <div class="top-menu">
            <q-btn flat color="dark" label="Home" to="/" />
            <q-btn flat color="dark" label="About" to="/about" />
            <q-btn flat color="dark" label="Explore" to="/explore" />
            <q-btn flat color="dark" label="Collection" to="/collection" />
        </div>
        <div class="toggle lt-sm"  @click="onOpenToggle">
            <div class="nav-icon">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
      </div>
   </nav>
</template>

<script>
export default {
  props: {
    value: Boolean
  },
  data () {
    return {
      open: false
    }
  },
  methods: {
    onOpenToggle () {
      this.$emit('input', !this.value)
      this.open = !this.open
      console.log('click')
    }
  }
}
</script>

<style>
.wrapper {
    margin: 0 auto;
    max-width: 960px;
    padding-left: 1rem;
    position: relative;
}
.top-bar {
    padding: 1rem 0;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 4000;
}
.top-bar a {
    text-decoration: none;
    color: var(--q-color-dark);
    background: #FFF;
}
.top-bar .brand {
    font-size: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.1rem;
    line-height: 1.05;
}
.top-bar .top-menu {
    display: none;
}
.top-bar.open .top-menu {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;    border-bottom: 1px solid var(--q-color-dark) ;
}
.top-bar .top-menu .item {
    width: 100%;
    text-align: center;
    padding: 1rem;
    text-transform: uppercase;
}
.toggle {
    position: absolute;
    right: 1rem;
    top: 0;
}

.nav-icon {
  width: 1.2rem;
  height: 25px;
  position: relative;
  margin: 0 auto;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: .5s ease-in-out;
  -moz-transition: .5s ease-in-out;
  -o-transition: .5s ease-in-out;
  transition: .5s ease-in-out;
  cursor: pointer;
}

.nav-icon span {
  display: block;
  position: absolute;
  height: 2px;
  width: 100%;
  background: var(--q-color-dark);
  opacity: 1;
  left: 0;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: .25s ease-in-out;
  -moz-transition: .25s ease-in-out;
  -o-transition: .25s ease-in-out;
  transition: .25s ease-in-out;
}

.nav-icon span:nth-child(1) {
  top: 3px;
}

.nav-icon span:nth-child(2) {
  top: 10px;
}

.nav-icon span:nth-child(3) {
  top: 17px;
}

.open .nav-icon span:nth-child(1) {
  top: 10px;
  -webkit-transform: rotate(135deg);
  -moz-transform: rotate(135deg);
  -o-transform: rotate(135deg);
  transform: rotate(135deg);
}

.open .nav-icon span:nth-child(2) {
  opacity: 0;
  right: -60px;
}

.open .nav-icon span:nth-child(3) {
  top: 10px;
  -webkit-transform: rotate(-135deg);
  -moz-transform: rotate(-135deg);
  -o-transform: rotate(-135deg);
  transform: rotate(-135deg);
}
@media screen and (min-width: 600px) {
.wrapper {
    margin: 0 auto;
    max-width: 960px;
    padding-left: 1rem;
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.top-bar .top-menu {
    display: flex;
    flex-direction: row;
    ---align-items: center;
  }
}
</style>
