<script>
</script>

<div class="home">
  <div class="homeText">I am Naveen.<br />I am a Web Developer.</div>
  <div class="image"><img src="assets/images/main.svg" alt="Main" /></div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Allura&display=swap");
  .home {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 88vh;
    padding: 10px;
  }

  .image {
    flex: 1;
  }

  .image img {
    display: block;
    width: 80%;
    margin: auto;
  }

  .homeText {
    font-family: "Allura", cursive;
    flex: 1;
    height: 100%;
    text-align: center;
    color: whitesmoke;
    font-size: 80px;
    font-weight: 500;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @media screen and (max-width: 900px) {
    .home {
      flex-direction: column;
      margin-top: 100px;
    }

    .image {
      margin-top: 15px;
    }
  }
</style>
