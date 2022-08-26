<script>
  import Project from "./Project.svelte";

  let html = "assets/images/html.png";
  let css = "assets/images/css.png";
  let js = "assets/images/javascript.png";
  let react = "assets/images/react.png";
  let redux = "assets/images/redux.png";
  let nodejs = "assets/images/nodejs.png";
  let express = "assets/images/express.png";
  let mongodb = "assets/images/mongodb.png";
</script>

<div>
  <div class="projectsTitle">Projects</div>
  <div class="projectsContainer">
    <Project
      img="assets/images/books.jpg"
      name="Converse"
      github="https://github.com/naveen0-0/converseclient"
      live="https://converse-1910.netlify.app/"
      techUsed={[html, css, js, react, redux, nodejs, express, mongodb]}
    />
    <Project
      img="assets/images/blogposter.png"
      name="FullStack Blog"
      github="https://github.com/naveen0-0/realblogclient/"
      live="https://blogreal.netlify.app"
      techUsed={[html, css, js, react, redux, nodejs, express, mongodb]}
    />
    <Project
      img="assets/images/newspaper.jpg"
      name="News"
      github="https://github.com/naveen0-0/news"
      live="https://newsroll.netlify.app/"
      techUsed={[html, css, js, react]}
    />
    <Project
      img="assets/images/movie.jpg"
      name="Movie"
      github="https://github.com/naveen0-0/newmovie"
      live="https://mynori.netlify.app/"
      techUsed={[html, css, js, react]}
    />
    <Project
      img="assets/images/shoppp.png"
      name="FullStack Shoppp"
      github="https://github.com/naveen0-0/ecommerceclient"
      live="https://xhoppie.netlify.app/"
      techUsed={[html, css, js, react, redux, nodejs, express, mongodb]}
    />
    <Project
      img="assets/images/covid.jpg"
      name="Covid Tracker"
      github="https://github.com/naveen0-0/trackerc19"
      live="https://trackerc19.netlify.app/"
      techUsed={[html, css, js, react]}
    />
  </div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap");
  /* @ Projects */
  .projectsTitle {
    font-size: 32px;
    margin: 0px 0px 20px;
    padding: 25px 25px 10px;
    text-align: center;
    font-weight: bold;
    color: whitesmoke;
    font-family: "Fira Code";
  }

  .projectsContainer {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    width: 85%;
    margin: 0px auto 10px;
    gap: 30px;
  }
</style>
