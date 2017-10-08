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
        <div>
          <h1 class="heading">Nick Summers</h1>
          <h2 class="tagline">Developer, Designer, Lorem Ipsum</h2>
        </div>
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

#index { width: 100%; height: 100%; }

.landing-container {
  background: #ffffff; /* Old browsers */
  background: -moz-linear-gradient(-45deg,  #ffffff 0%, #ffffff 75%, #414042 100%); /* FF3.6-15 */
  background: -webkit-linear-gradient(-45deg,  #ffffff 0%,#ffffff 75%,#414042 100%); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(135deg,  #ffffff 0%,#ffffff 75%,#414042 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#414042',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */

  width: 100%; height: 100%;

  position: relative;

  padding: 20px 40px;

  box-sizing: border-box;

  display:flex;
  flex-direction: column;

  header {
    width: 100%; height: 60px;
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
    display: flex;
    flex-grow: 1;

    transition: all .5s;

    position: relative;
    div {
      position: absolute;
      bottom: 0; left: 0;

      margin: 0 0 40px 0;
    }

    .heading {
      font: 60px $oswald;
      @include bp (lg) { font-size: 76px; }
      @include bp (xxlg) { font-size: 90px; }

      color: #333;

      margin: 0; padding: 0;

      transition: all .5s;
    }

    .tagline {
      font: 32px $roboto;
      @include bp (lg) { font-size: 48px; }
      @include bp (xxlg) { font-size: 60px; }

      color: #333;

      margin: 0; padding: 0;

      transition: all .5s;
    }
  }
}

.work-container {
  background: #333;

  padding: 60px 40px;

  h1 {
    margin: 0 auto 40px auto; padding: 0;

    color: #fff;

    font: 60px $roboto;
    @include bp(lg) { font-size: 80px; }

    text-align: left;
  }

  .projects {

    margin: 0 auto; padding: 0;

    ul {
      margin: 0; padding: 0;

      list-style-type: none;

      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;

      li {
        width: 100%; height: 400px;
        @include bp(md) { width: 48%; height: 500px; }
        @include bp(lg) { width: 32.3333%; height: 600px; }
        @include bp(xxlg) { width: 24.25%; height: 700px; }

        margin: 20px 0 0 0;

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
          font-family: $oswald;

          position: absolute;
          right: 0;

          font-size: 60px; bottom: -16px;
          @include bp(md) { font-size: 80px; bottom: -22px; }
          @include bp(xxlg) { font-size: 100px; bottom: -28px; }
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
