<template>
  <div id="maps">
    <article class="project">
      <header>
        <h1><a href="https://maps.msu.edu/interactive">MSU Campus Maps</a></h1>
      </header>
      <div class="project-description">
        <div class="project-description-left">
          <h2>Beginners Luck</h2>

          <p class="description">MSU Campus Maps was my first and last contribution as a student developer. Its quite crazy to think that over the course of 3 years I saw the maps site rapidly change designs and have new features introduced on a regular basis. It is also crazy to think that my <b> first </b> assignment was to add construction polylines and polyfills on to the map. You know, no big deal for a developer who has never created an actual website much less a website that can have upwards of 10,000 users a day.</p>

          <p class="description">With so many users touching the site, not to mention my complete lack of knowledge of web design, I always wondered why I was chosen. Why I got the job over any of the other students that were attending MSU at the time. A couple years later, I finally got up the courage and asked. "Why Me? What did you see in me?"</p>

          <q>There were many other candidates that I could have chosen, but I saw that you had determination and drive.</q>

          <p class="description">I was and still am very humbled by that response, and I do believe it is one of my best qualties. The drive to never give up on a task and see it through to completion. </p>

          <p class="description">But enough about me. We're here to see the changes during my time during MSU. So without further ado.. </p>
        </div>
        <div class="project-description-right">
          <h2>Project Details</h2>

          <p class="details">Created For: Michigan State University</p>
          <p class="details">Last Contribution: 5/31/2017</p>
          <p class="details">Status: Completed</p>

          <h2>Skills Used</h2>

          <ul>
            <li>HTML5</li>
            <li>Sass</li>
            <li>Javascript</li>
            <li>jQuery</li>
            <li>PHP</li>
            <li>Gulp</li>
            <li>Gitlab</li>
            <li>Google Maps API</li>
            <li>Google Analytics</li>
          </ul>
        </div>
      </div>
      <div class="images">
        <img src="../assets/imgs/interactive-map-2014.png" alt="MSU Campus Interactive Map 2014">
        <p class="description">MSU Campus Map in 2014. Even has my first feature!</p>
        <img src="../assets/imgs/interactive-map-2015.jpg" alt="MSU Campus Interactive Map 2015">
        <img src="../assets/imgs/interactive-map-2017.jpg" alt="MSU Campus Interactive Map 2017">
      </div>
    </article>
  </div>
</template>

<script>
export default {
  name: 'maps',
  data () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/main";

#maps {
  width: 100%; height: 100%;
}

.project {
  width: 100%; height: 100%;

  display: grid;

  header {
    height: 500px;

    // background-image: url("../assets/imgs/MapsAside-Med.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 50% 50%;

    position: relative;

    h1 {
      font: 72px $oswald;

      color: #fff;

      margin: 0; padding: 0;

      width: 100%; height: 100%;

      position: absolute;

      background: rgba(46,196,182, .8);

      display: flex;
      justify-content:center;
      align-content:center;
      flex-direction:column;
      text-align: center;

      a {
        text-decoration: none;

        color: #fff;

        &:hover {
          text-decoration: underline;
        }
      }
    }
  }

  &-description {
    display: grid;
    grid-template-columns: 2fr 1fr;

    max-width: 1200px;

    margin: 0 auto;

    &-left, &-right {
      margin: 10px; padding: 10px;
    }
    h2 {
      font: 48px $oswald;

      color: #2EC4B6;

      margin: 20px 0; padding: 0;
    }

    p.details {
      font: italic 300 18px $roboto;

      color: #333;

      margin: 0;

      &:first-child { margin-top: 1em; }
      &:last-child { margin-bottom: 1em; }
    }

    p.description {
      font: 300 18px $roboto;
      line-height: 30px;

      color: #333;
    }

    q {
      font: italic 300 24px $roboto;
      line-height: 30px;

      color: #E71D36;
    }

    ul {
      list-style-type: bullet;

      margin: 1em 0; padding: 0 0 0 20px;

      &:after {
        content: "";
        display: table;
        clear: both;
      }

      li {
        font: 300 18px $roboto;
        line-height: 30px;

        color: #333;

        float: left;

        width: 50%;

        text-align: left;
      }
    }
  }

  .images {
    width: 100%;

    img {
      display: block;

      max-width: 1200px;

      margin: 20px auto 0 auto;

      border: 2px solid #B2DBBF;
    }

    .description {
      font: 300 18px $roboto;
      line-height: 30px;

      color: #333;

      border-bottom: 1px solid #333;

      max-width: 1200px;

      margin: 10px auto 20px auto;
    }
  }

}
</style>
