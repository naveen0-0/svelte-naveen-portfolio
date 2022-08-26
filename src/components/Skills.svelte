<script>
  import Skill from "./Skill.svelte";
</script>

<div>
  <div class="skillTitle">Skills</div>
  <div class="skillsContainer">
    <Skill img="assets/images/html.png" name="Html" />
    <Skill img="assets/images/css.png" name="Css" />
    <Skill img="assets/images/javascript.png" name="Javascript" />
    <Skill img="assets/images/bootstrap.png" name="Bootstrap" />
    <Skill img="assets/images/jquery.png" name="Jquery" />
    <Skill img="assets/images/sass.png" name="Sass" />
    <Skill img="assets/images/react.png" name="React" />
    <Skill img="assets/images/redux.png" name="redux" />
    <Skill img="assets/images/nodejs.png" name="NodeJS" />
    <Skill img="assets/images/express.png" name="Express" />
    <Skill img="assets/images/mongodb.png" name="MongoDB" />
  </div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap");
  .skillTitle {
    font-size: 32px;
    margin: 0px 0px 20px;
    text-align: center;
    padding: 25px 25px 10px;
    font-weight: bold;
    color: whitesmoke;
    font-family: "Fira Code";
  }

  .skillsContainer {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    width: 80%;
    margin: 0px auto 10px;
    gap: 20px;
  }
</style>
