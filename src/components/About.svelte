<script>
  import { getTime } from "../utils/utils";
</script>

<div class="about">
  <div class="aboutTitle">About Me</div>
  <div class="aboutDescription">
    <p>
      I am Naveen Kumar Reddy. I live in Andhra Pradesh. I am a Full Stack
      Javascript Developer, with experience in React, Nodejs and MongoDB.I
      consider myself a forever student. I actually find joy in learning and
      doing new things.
    </p>
    <p>
      I like cricket, football and tennis. During these corona days, i picked up
      chess as a hobby and started to get good at it.
    </p>
    <p>
      I started to learn programming {getTime()} years ago. I initially went into
      data scientist route and started to learn python and played with Numpy module.
      But, I switched to wev development because, working with numbers is kind of
      boring. I prefered to work in the creative field.
    </p>

    <p>I also do have some beginner experience in languages like C++,Java.</p>
  </div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap");
  /* * About component */
  .aboutTitle {
    font-size: 32px;
    font-weight: bold;
    text-align: center;
    padding: 10px 10px 5px;
    margin: 10px 0px 20px;
    color: whitesmoke;
    font-family: "Fira Code";
  }

  .aboutDescription {
    width: 80%;
    margin: auto;
    padding: 20px;
    background-color: rgb(34, 34, 37);
    box-shadow: 3px 2px 2px #111;
    border-radius: 5px;
    font-size: 16px;
    font-family: "Fira Code";
  }

  .aboutDescription p {
    text-indent: 20px;
    padding: 20px;
    color: rgb(187, 183, 183);
    font-family: "Fira Code";
  }

  @media screen and (max-width: 450px) {
    .aboutDescription {
      width: 95%;
    }
  }
</style>
