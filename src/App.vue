<template>
  <div id="app">
    <div id="home" class="canvas">
      <ul id="scene" data-friction-x="0.03" data-friction-y="0.05">
        <li class="layer" id="specks" data-depth="0.1"></li>
        <li class="layer" id="layer-1" data-depth="0.15">
          <div class="img" id="img-1"></div>
        </li>
        <li class="layer" id="layer-2" data-depth="0.25">
          <div class="img" id="img-2"></div>
        </li>
        <li class="layer" id="layer-3" data-depth="0.45">
          <div class="img" id="img-3"></div>
        </li>
      </ul>
      <div
        class="container is-fluid is-flex"
        style="height:100%; flex-direction:column; justify-content: center;"
      >
        <h1 class="title has-text-white is-1 is-size-2-mobile">
          Hi, I'm
          <span class="title is-1 is-size-2-mobile has-text-danger"
            >Scott Ames</span
          >.
        </h1>
        <h2 class="subtitle has-text-white is-3 is-size-4-mobile">
          I'm a full stack web developer.
        </h2>
        <div class="buttons is-centered">
          <a
            v-scroll-to="'#about'"
            class="button is-primary has-text-weight-medium is-family-secondary"
            style="z-index:99999;"
          >
            ABOUT ME
          </a>

          <a
            v-scroll-to="{ el: '#projects', duration: 1000 }"
            class="button is-danger is-family-secondary has-text-weight-medium"
            style="z-index:99999;"
          >
            VIEW MY WORK
          </a>
        </div>
      </div>
    </div>
    <About />
    <Navbar />

    <Projects />

    <Contact />
    <div class="footer">
      <div class="level is-mobile mb-4">
        <div class="level-item">
          <div class="link-wrap mx-4">
            <a target="_blank" href="https://www.github.com/scottaames">
              <span class="icon is-large has-text-grey-lighter">
                <i class="fab fa-lg fa-github"></i>
              </span>
            </a>
          </div>
        </div>
        <div class="level-item">
          <div class="link-wrap mx-4">
            <a
              target="_blank"
              href="https://www.linkedin.com/in/scott-ames-16763852/"
            >
              <span class="icon is-large has-text-grey-lighter">
                <i class="fab fa-lg fa-linkedin-in"></i>
              </span>
            </a>
          </div>
        </div>
        <div class="level-item">
          <div class="link-wrap mx-4">
            <a target="_blank" href="https://www.instagram.com/scottyames">
              <span class="icon is-large has-text-grey-lighter">
                <i class="fab fa-lg fa-instagram"></i>
              </span>
            </a>
          </div>
        </div>
      </div>
      <div class="content">
        Built by Scott Ames with
        <a class="is-inline has-text-info" href="https://www.vuejs.com"
          >Vue.js</a
        >
        and
        <a class="is-inline has-text-info" href="https://www.bulma.io">Bulma</a>
      </div>
    </div>
  </div>
</template>

<script>
import About from '@/views/About.vue'
import Projects from '@/views/Projects.vue'
import Contact from '@/views/Contact.vue'
import Navbar from '@/components/NavBar.vue'

export default {
  name: 'App',
  components: {
    About,
    Projects,
    Contact,
    Navbar,
  },
}
</script>

<style lang="sass"></style>
