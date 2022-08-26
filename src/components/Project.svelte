<script>
  export let img;
  export let name;
  export let github;
  export let live;
  export let techUsed;
</script>

<div class="project">
  <div class="projectName">{name}</div>
  <img src={img} alt={name} class="projectImage" />

  <div class="techUsed">Tech used</div>
  <div class="techs">
    {#each techUsed as tech, index}
      <div key={index} class="tech">
        <img src={tech} alt="Tech" class="techImage" />
      </div>
    {/each}
  </div>

  <div class="projectLinks">
    <a
      href={github}
      target="_blank"
      rel="noopener noreferrer"
      title="View Code"
    >
      <img src="assets/images/github.png" alt="Github" />
    </a>
    <a href={live} target="_blank" rel="noopener noreferrer" title="Go to Site">
      <img src="assets/images/live.png" alt="Live" />
    </a>
  </div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap");

  .projectName {
    font-size: 22px;
    padding: 5px;
    text-align: center;
    font-family: "Fira Code";
    color: whitesmoke;
  }

  .project {
    background-color: #222;
    box-shadow: 3px 3px 3px #111;
    border-radius: 10px;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    position: relative;
  }

  .project img {
    width: 200px;
    height: 100px;
    display: block;
    margin: auto;
    border-radius: 5px;
  }

  .projectLinks {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 200px;
    margin: auto;
    padding: 10px;
  }

  .projectLinks img {
    width: 25px;
    height: 25px;
  }

  .techs {
    background-color: #111;
    padding: 5px;
    border-radius: 5px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(30px, 1fr));
  }

  .tech {
    text-align: center;
    font-family: "Fira Code";
    font-size: 12px;
    padding: 3px;
    border-radius: 10px;
    color: rgb(182, 182, 182);
    display: inline-block;
  }

  .techUsed {
    font-family: "Fira Code";
    text-align: center;
    color: rgb(205, 205, 206);
    margin: 10px 0px;
  }

  .techImage {
    display: block;
    width: 25px !important;
    height: 25px !important;
    object-fit: cover;
  }
</style>
