<template>
  <div>
    <section id="about" class="hero is-medium is-dark" style="background-color: hsl(0, 0%, 8%)">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title is-spaced">Our Projects</h1>
          <h2 class="subtitle">
            We deliver quality projects <strong>regularly</strong>. Here are some of them.
          </h2>
        </div>
      </div>
    </section>

    <div class="c-projects__showcase tile">
      <div class="tile is-12 is-vertical ">
        <figure class="c-projects__thumbnail image tile" @click="openUrl('https://fotoolkit.com')">
          <img src="@/assets/images/projects/fotoolkit.jpg" alt="FOToolkit">
          <figcaption class="has-text-centered">
            <h2 class="title">FOToolkit</h2>
            <p class="subtitle">Full function FIBOS web wallet toolkit.</p>
          </figcaption>
        </figure>

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'projects-showcase',
    methods: {
      openUrl (url) {
          window.open(url)


        return false
      }
    }
  }
</script>

<style lang="scss" scoped>
  .c-projects__showcase {
    background-color: black;
  }

  .c-projects__thumbnail {
    position: relative;
    overflow: hidden;
    height: 100%;
    cursor: pointer;

    img {
      object-fit: cover;
      height: 100%;
      transition: opacity 0.5s, transform 0.5s, filter 0.5s;
    }

    &:hover img {
      opacity: 0.4;
      filter: blur(2px);
    }

    figcaption {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      transition: opacity 0.5s;
      opacity: 0;
    }

    &:hover figcaption {
      opacity: 1;
    }

    .title {
      margin: 0 0 1em;
      background: rgba(0, 0, 0, 0.9);
      color: white;
      text-transform: uppercase;
      font-weight: 500;
      transition: margin 0.35s;
    }

    .subtitle {
      display: inline-block;
      margin: 0 0 0.25em;
      padding: 0.4em 1em;
      background: rgba(255, 255, 255, 0.9);
      color: black;
      font-weight: 500;
    }

    .title, .subtitle {
      display: inline-block;
      padding: 0.4em 1em;
      box-shadow: 0 1px 10px rgba(0,0,0,0.2);
    }

    &:hover .title {
      margin: 0 0 0.25em;
    }
  }
</style>
