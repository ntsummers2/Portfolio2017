<template>
  <div id="index">
    <section class="landing-container">
      <header>
        <nav>
          <input type="checkbox" id="nav-trigger" class="nav-trigger" />
          <label for="nav-trigger"><i class="fa fa-bars fa-2x" aria-hidden="true"></i></label>
          <ul class="nav-container">
            <li> <a href="#Projects">Projects</a> </li>
            <li> <a href="#Experience">Experience</a> </li>
            <li> <a href="#Connect">Connect</a> </li>
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
    <section class="work-container" id="Projects">
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

    <section class="experience-container" id="Experience">

      <h1> Experience </h1>

      <h2> Information Technology Professional </h2>
      <h3> Michigan State University: IT Services VP And CIO </h3>
      <h4> May 2017 - Present</h4>

      <p class="description">As part of a 6 month rotational program under the CIO, helped create, manage, and update MSU applications and websites using VueJS and Java. Met with clients to determine product needs, designed wireframes, and implemented solutions upon clients approval. Cleared up accessibility issues and redesiged elements to be more user friendly. </p>
      <p class="achievement-header"> Achievements: </p>
      <ul class="achievement-list">
          <li>Took over front-end work on Travelregistry.msu.edu and saw project to launch across web, iOS, and android platforms.</li>
      </ul>

      <div class="border"></div>

      <h2> Student Programmer </h2>
      <h3> Michigan State University: IT Services Content and Collaboration</h3>
      <h4> January 2014 - May 2017</h4>

      <p class="description">Create, manage, and update high-visibility MSU websites with extensive use of full-stack development. Optimize sites for SEO, introduce responsive design, and hold sites to AA accessibility compliance. Extensive use of Google Maps API, Google Analytics, and MSU API’s.</p>
      <p class="achievement-header"> Achievements: </p>
      <ul class="achievement-list">
          <li>Worked on MSU Search Services which consist of 5 web properties averaging over 400,000 sessions per month.</li>
          <li>Completely rewrote and redesigned Maps.msu.edu from the ground up.</li>
      </ul>

      <div class="border"></div>

      <h2> IT Intern </h2>
      <h3> Kellogg </h3>
      <h4> May 2015 - August 2015</h4>

      <p class="description">Project manager and led teams to success on multiple projects such as the creation of an API to be used by Kellogg’s IT team. Introduced gamification to increase customer service among the global employee help desks. Created wireframes, empathy maps, and personas to increase usability of current Kellogg websites. Taught 40 8th grade middle school students on thermodynamics.</p>
      <p class="achievement-header"> Achievements: </p>
      <ul class="achievement-list">
          <li>Oversaw, designed and created an API to help transition Kellogg’s servers to Amazon Web Services.</li>
          <li>Designed wireframes for Kellogg’s internal global employee website that was approved by the CIO.</li>
      </ul>
    </section>

    <section class="connect-container" id="Connect">
      <h1>Connect</h1>
      <ul>
        <li>
          <a href="https://codepen.io/ntsummers1/" aria-label="Go To Codepen Profile">
            <div class="fa fa-codepen" aria-hidden="true"></div>
            <div class="icon-title">Codepen</div>
          </a>
        </li>
        <li>
          <a href="https://github.com/ntsummers2" aria-label="Go To Github Profile">
            <div class="fa fa-github" aria-hidden="true"></div>
            <div class="icon-title">Github</div>
          </a>
        </li>
        <li>
          <a href="www.linkedin.com/in/nicholas-summers-454329aa" aria-label="Go To LinkedIn Profile">
            <div class="fa fa-linkedin" aria-hidden="true"></div>
            <div class="icon-title">Codepen</div>
          </a>
        </li>
      </ul>

      <p>Interested? Shoot me an email at: <a href="mailto:ntsummers2@gmail.com">ntsummers2@gmail.com</a></p>
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
  background: #ffffff;
  background: -moz-linear-gradient(-45deg,  #ffffff 0%, #ffffff 75%, #414042 100%);
  background: -webkit-linear-gradient(-45deg,  #ffffff 0%,#ffffff 75%,#414042 100%);
  background: linear-gradient(135deg,  #ffffff 0%,#ffffff 75%,#414042 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#414042',GradientType=1 );

  width: 100%; height: 100%;
  max-height: 80%;

  position: relative;

  padding: 20px 40px;

  box-sizing: border-box;

  display:flex;
  flex-direction: column;

  header {
    position: absolute;
    top: 0; left: 0;

    width: 100%;

    z-index: 1;

    @include bp(md) {
      position: relative;
      top: auto; left: auto;
    }


    nav {

      .nav-trigger {
        position: absolute;
        clip: rect(0, 0, 0, 0);

        display: block;
        @include bp(md) {display: none;}
      }

      label[for="nav-trigger"] {
        position: absolute;
        right: 20px;top: 19px;

        display: block;
        @include bp(md) {display: none;}

        color: #333;

        cursor: pointer;
      }

      .nav-trigger:checked ~ .nav-container {
        box-shadow: 0 10px 5px 0px rgba(0, 0, 0, 0.5);
        @include bp(md) {box-shadow: none;}

        opacity: 1;

        display: inline-block;

      }


      ul {
        width: 100%;

        display: none;
        @include bp(md) { display: flex; }
        justify-content: center;

        list-style-type: none;
        padding: 0; margin: 0;

        text-align: center;
        li {
          width: 100%;
          @include bp(md) {
            width: auto;
          }

          display: inline-block;

          box-sizing:border-box;

          font: 32px $roboto;
          color: #595959;

          padding: 0 20px; margin: 20px 0;
          @include bp(md) {
            margin: 0;
          }

          border-right: 0;
          @include bp(md) {
            border-right: 2px solid #595959;
          }

          &:first-child {
            margin-top: 60px;
            @include bp(md) { margin-top: 0;}
          }

          &:last-child {
            border-right: 0;
          }

          a {
            transition: all .15s ease;

            text-decoration: underline;

            color: #595959;

            &:hover {
              transform: translateY(-1px);
              text-decoration: none;
            }
            &:active { transform: translateY(1px); }
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

    font: 60px $oswald;
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
          font-family: $roboto;

          position: absolute;
          right: 0;

          font-size: 60px; bottom: -14px;
          @include bp(md) { font-size: 72px; bottom: -17px; }
          @include bp(xxlg) { font-size: 84px; bottom: -20px; }
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
}

.experience-container {
  background: #fff;

  padding: 60px 40px;

  h1 {
    margin: 0 auto 40px auto; padding: 0;

    color: #333;

    font: 60px $oswald;
    @include bp(lg) { font-size: 80px; }

    text-align: left;
  }

  h2 {
    color: #333;

    font: 24px $roboto;
    @include bp(lg) { font-size: 32px; }

    margin: 5px 0;
  }

  h3 {
    color: #333;

    font: 18px $roboto;
    @include bp(lg) { font-size: 24px; }

    margin: 5px 0;
  }

  h4 {
    color: #333;

    font: 14px $roboto;
    @include bp(lg) { font-size: 16px; }

    margin: 5px 0;
  }

  p {
    color: #333;

    font: 12px $roboto;
    @include bp(lg) { font-size: 14px; }
  }

  ul {

    padding: 0 0 0 20px;

    li {
      color: #333;

      font: 12px $roboto;
      @include bp(lg) { font-size: 14px; }
    }
  }

  .border {
    border: 1px solid #333;

    margin: 20px 0 20px 0;
  }
}

.connect-container {
  background: #333;

  padding: 60px 40px;

  h1 {
    margin: 0 auto 40px auto; padding: 0;

    color: #fff;

    font: 60px $oswald;
    @include bp(lg) { font-size: 80px; }

    text-align: left;
  }

  p {
    margin: 40px 0;

    font: 20px $roboto;
    @include bp(lg) { font-size: 32px; }
    color: #fff;

    text-align: center;

    a {
      transition: all .15s ease;

      text-decoration: underline;

      color: #fff;

      &:hover {
        transform: translateY(-1px);
        text-decoration: none;
      }
      &:active { transform: translateY(1px); }
    }
  }

  ul {
    margin: 0; padding: 0;

    list-style-type: none;

    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;

    li {

      margin: 10px 10px 0 0;

      &:last-child {
        margin-right: 0;
      }

      a {
        display: block;

        height: 100%; width: 100%;

        transition: all .15s ease;

        text-decoration: none;

        &:hover { transform: translateY(-1px); }
        &:active { transform: translateY(1px); }

        div {
          display: block;

          color: #fff;

          font-size: 60px;
          @include bp(lg) { font-size: 80px; }

          text-align:center;
        }
      }

      .icon-title {
        font: 20px $roboto;
        @include bp(lg) { font-size: 32px; }
        color: #fff;

        text-align: center;
      }
    }
  }
}
</style>
