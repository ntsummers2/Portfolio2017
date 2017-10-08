<template>
  <div id="index">
    <section class="landing-container">
      <header>
        <nav>
          <ul>
            <router-link tag="li" to="/"><a>Work</a></router-link>
            <li>Logo</li>
            <router-link tag="li" to="/about"><a>About</a></router-link>
          </ul>
        </nav>
      </header>
      <div class="me">
        <h1 class="heading">Nicholas Summers</h1>
        <h2 class="tagline">Coder, Designer, UX + Accessibility Specialist.</h2>
      </div>
    </section>
    <section class="work-container">
      <h1>Projects</h1>
      <div class="projects">
        <ul>
          <router-link tag="li" to="/maps"><a></a></router-link>
          <li></li>
          <li></li>
          <li></li>
          <div class="clear"></div>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>

@import "../assets/styles/main";

#index { width: 100%; height: 100%;}

.clear { clear: both; }

.landing-container {
  background: #ffffff; /* Old browsers */
  background: -moz-linear-gradient(-45deg,  #ffffff 0%, #ffffff 75%, #414042 100%); /* FF3.6-15 */
  background: -webkit-linear-gradient(-45deg,  #ffffff 0%,#ffffff 75%,#414042 100%); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(135deg,  #ffffff 0%,#ffffff 75%,#414042 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#414042',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */

  width: 100%; height: 100%;

  position: relative;

  padding: 20px;

  box-sizing: border-box;

  header {
    nav {
      ul {
        display: flex;
        justify-content: center;

        list-style-type: none;
        padding: 0; margin: 0;

        text-align: center;
        li {
          display: inline-block;

          font: 32px $roboto;
          color: #595959;

          padding: 0 20px;

          &:nth-child(2) {
            border-left: 2px solid #595959; border-right: 2px solid #595959;
          }

          a {
            color: #595959;
            text-decoration: none;
          }
        }
      }
    }
  }

  .me {
    position: absolute;

    bottom: 120px; left: 120px;

    .heading {
      font: 5.5vw $oswald;

      color: #333;

      margin: 0; padding: 0;
    }

    .tagline {
      font: 3vw $roboto;

      color: #333;

      margin: 0; padding: 0;
    }
  }
}

.work-container {
  background: #333;

  padding: 60px 40px;

  h1 {
    margin: 0 auto 60px auto; padding: 0;

    color: #fff;

    font: 60px $roboto;

    text-align: right;

    max-width: 1600px;
  }

  .projects {

    max-width: 1600px;

    margin: 0 auto; padding: 0;

    ul {
      margin: 0; padding: 0;

      list-style-type: none;

      li {
        width: 24.25%; height: 700px;

        display: block; float: left;

        margin-right: 1%;

        position: relative;

        transition: all .3s ease;

        &:before {
          transition: all .3s ease;
          background: rgba(0,0,0,0);
          content: "";
          display: block;
          width: 100%; height: 100%;
        }
        &:after {
          transition: all .2s ease;
          opacity: 0;
          content: "";
          display: block;
          color: #fff;
          font: 100px $oswald;
          position: absolute;
          bottom: -29px; right: 0;
        }

        &:hover {
          cursor: pointer;
          &:before { background: rgba( 0, 0, 0, .5); }

          &:after { opacity: 1; }
        }

        &:nth-child(1) {
          background: #f7f7f7;

          &:hover:after { content: "Maps"; }
        }
        &:nth-child(2) {
          background: #f7f7f7;

          &:hover:after { content: "Search"; }
        }
        &:nth-child(3) {
          background: #f7f7f7;

          &:hover:after { content: "Campus"; }
        }
        &:nth-child(4) {
          background: #f7f7f7;

          margin-right: 0;

          &:hover:after { content: "Travel"; }
        }

        a {
          display: block;

          width: 100%; height: 100%;

          position: absolute;
          top: 0;
        }
      }
    }
  }

  footer {

  }
}
</style>
