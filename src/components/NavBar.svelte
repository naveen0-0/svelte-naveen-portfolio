<script>
  import { link } from "svelte-spa-router";
  let dropdownOpen = true;
  const ToggleDropDown = () => (dropdownOpen = !dropdownOpen);
  const closeDropDown = () => (dropdownOpen = true);
</script>

<div class="navbar">
  <div class="title">
    <a href="/" use:link class="titleText">Naveen</a>
  </div>

  <div class={dropdownOpen ? "links" : "showLinks"}>
    <div class="navbarlink" on:click={closeDropDown}>
      <a href="/about" use:link>about</a>
    </div>

    <div class="navbarlink" on:click={closeDropDown}>
      <a href="/skills" use:link>skills</a>
    </div>

    <div class="navbarlink" on:click={closeDropDown}>
      <a href="/projects" use:link>projects</a>
    </div>

    <div class="navbarlink" on:click={closeDropDown}>
      <a href="/contact" use:link>contact</a>
    </div>

    <a
      href="assets/pdfs/resume.pdf"
      class="resume"
      target="_blank"
      download={true}>Resume</a
    >
  </div>

  <div class="burger" on:click={ToggleDropDown}>
    <div class="line" />
    <div class="line" />
    <div class="line" />
  </div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Allura&display=swap");
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code&display=swap");

  .navbar {
    background-color: #191d1d;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px;
    position: sticky;
    top: 0px;
    z-index: 100;
  }

  .title {
    text-decoration: none;
    padding: 0px 20px;
  }

  .titleText {
    font-family: "Allura", cursive;
    font-size: 3rem;
    background: linear-gradient(
      to right,
      #845ec2,
      #d65db1,
      #ff6f91,
      #ff9671,
      #ffc75f,
      #f9f871
    );

    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-size: 400%;
    animation: bg-animate 10s infinite alternate;
    cursor: pointer;
  }

  @keyframes bg-animate {
    0% {
      background-position: left;
    }

    100% {
      background-position: right;
    }
  }

  .links {
    background-color: green;
    z-index: 2;
    position: absolute;
    top: 80px;
    right: 10px;
    background-color: rgb(128, 128, 128);
    height: 150px;
    width: 100px;
    border-radius: 3px;
    display: none;
    flex-direction: column;
    justify-content: space-around;
    text-align: center;
  }

  .showLinks {
    background-color: green;
    z-index: 2;
    position: absolute;
    top: 80px;
    right: 10px;
    background-color: rgb(87, 87, 87);
    height: 200px;
    width: 130px;
    border-radius: 3px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    text-align: center;
  }

  .navbarlink {
    text-decoration: none;
    color: whitesmoke;
    font-size: 14px;
    font-family: "Fira Code";
    cursor: pointer;
  }

  .resume {
    background: linear-gradient(to top left, darkblue, royalblue);
    width: 100px;
    color: whitesmoke;
    padding: 5px 10px;
    text-decoration: none;
    border-radius: 999999999px;
    font-family: "Fira Code";
    font-size: 13px;
    transition: all 0.2s cubic-bezier(0.165, 0.84, 0.44, 1);
  }

  .resume:active {
    background: linear-gradient(to top right, salmon, cornflowerblue);
  }

  .burger {
    width: 30px;
    height: 18px;
    /* background-color: crimson; */
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    cursor: pointer;
  }

  .line {
    width: 20px;
    height: 2px;
    background-color: whitesmoke;
    margin: auto;
  }

  @media screen and (min-width: 900px) {
    .burger {
      display: none;
    }

    .links {
      z-index: 2;
      position: static;
      background-color: transparent;
      height: inherit;
      flex: 1;
      display: flex;
      flex: 1;
      flex-direction: column;
      justify-content: space-around;
      flex-direction: row;
    }

    .showLinks {
      z-index: 2;
      position: static;
      background-color: transparent;
      height: inherit;
      flex: 1;
      border-radius: 3px;
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
    }
  }
</style>
