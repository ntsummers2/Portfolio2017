<template>
  <div id="maps">
    <article class="project">
      <div class="project-content">
        <h1>Lorem Ipsum</h1>
        <p class="details">Created For: Michigan State University</p>
        <p class="details">Last Contribution: 5/31/2017</p>
        <p class="details">Status: Completed</p>

        <p class="description">Bacon ipsum dolor amet frankfurter tail short loin hamburger filet
          mignon kevin cupim sausage tongue bacon. Pork chop swine ham hock,
          jerky short loin andouille leberkas salami prosciutto shoulder short
          ribs pancetta doner. Shoulder cupim tri-tip pork belly chicken andouille
          flank kevin, alcatra ribeye. Beef jowl turducken, chicken ball tip
          fatback ground round tenderloin strip steak capicola kielbasa. Jerky
          picanha pork belly, beef ribs ribeye tongue biltong andouille ham hock
          capicola sausage. Drumstick kielbasa capicola turkey fatback.</p>

        <p class="description">Bacon ipsum dolor amet frankfurter tail short loin hamburger filet
          mignon kevin cupim sausage tongue bacon. Pork chop swine ham hock,
          jerky short loin andouille leberkas salami prosciutto shoulder short
          ribs pancetta doner. Shoulder cupim tri-tip pork belly chicken andouille
          flank kevin, alcatra ribeye. Beef jowl turducken, chicken ball tip
          fatback ground round tenderloin strip steak capicola kielbasa. Jerky
          picanha pork belly, beef ribs ribeye tongue biltong andouille ham hock
          capicola sausage. Drumstick kielbasa capicola turkey fatback.</p>

        <p class="description">Bacon ipsum dolor amet frankfurter tail short loin hamburger filet
          mignon kevin cupim sausage tongue bacon. Pork chop swine ham hock,
          jerky short loin andouille leberkas salami prosciutto shoulder short
          ribs pancetta doner. Shoulder cupim tri-tip pork belly chicken andouille
          flank kevin, alcatra ribeye. Beef jowl turducken, chicken ball tip
          fatback ground round tenderloin strip steak capicola kielbasa. Jerky
          picanha pork belly, beef ribs ribeye tongue biltong andouille ham hock
          capicola sausage. Drumstick kielbasa capicola turkey fatback.</p>

        <h2>Skills Used/Learned</h2>
        <ul>
          <li>HTML5</li>
          <li>Sass</li>
          <li>Javascript</li>
          <li>jQuery</li>
          <li>PHP</li>
          <li>Gulp</li>
          <li>Gitlab</li>
        </ul>
        <h2>Lorem Ipsum</h2>
      </div>
      <aside class="project-image"></aside>
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

    &-content {
      width: 66.6666%;

      float: left;

      padding: 40px;

      box-sizing: border-box;

      display: inline-block;

      h1 {
        font: 60px $oswald;

        color: #333;

        margin: 0; padding: 0;
      }

      p.details {
        font: 18px $roboto;
        font-style: italic;

        color: #333;

        margin: 0;

        &:first-child { margin-top: 1em; }
        &:last-child { margin-bottom: 1em; }
      }

      p.description {
        font: 18px $roboto;

        color: #333;
      }

      h2 {
        font: 32px $oswald;

        color: #333;

        margin: 0; padding: 0;
      }

      ul {
        list-style-type: none;

        margin: 1em 0; padding: 0;

        &:after {
          content: "";
          display: table;
          clear: both;
        }

        li {
          float: left;

          width: 14.28571%;

          text-align: center;
        }
      }
    }

    &-image {
      width: 33.3333%; height: 100%;

      float: left;

      display: inline-block;

      background-image: url("https://unsplash.it/g/1000/1800/");
      background-size: cover;
      background-repeat: no-repeat;
      background-position: 50% 50%;

      &:after {
        content: "";
        display: table;
        clear: both;
      }
    }
}
</style>
