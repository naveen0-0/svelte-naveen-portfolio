<script>
  export let img;
  export let name;
</script>

<div class="skill">
  <img src={img} alt={name} class="skillImage" />
  <div class="skillName">{name}</div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap");
  .skillImage {
    width: 70px;
    display: block;
    margin: auto;
  }

  .skillName {
    font-size: 18px;
    text-align: center;
    font-family: "Fira Code";
    color: whitesmoke;
  }

  .skill {
    background-color: #eee;
    box-shadow: 3px 3px 3px #111;
    padding: 20px;
    border-radius: 10px;
    background-color: #222;
  }
</style>
