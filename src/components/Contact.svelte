<script>
  import emailjs from "@emailjs/browser";
  let submitting = false;
  let name = "";
  let email = "";
  let subject = "";
  let message = "";

  const sendMail = () => {
    submitting = true;

    const template = {
      name: name,
      email: email,
      subject: subject,
      message: message,
    };

    emailjs
      .send(
        "service_yvsd6pm",
        "template_zc080aa",
        template,
        "p4D5uyCTOzuEE75ss"
      )
      .then(() => {
        name = "";
        email = "";
        subject = "";
        message = "";
        setMailSent(true);
      })
      .catch((err) => console.log("Error,", err))
      .finally(() => {
        submitting = false;
      });
  };
</script>

<div class="formContainer">
  <div class="formTitle">Contact Form</div>

  <form on:submit|preventDefault={sendMail} method="POST" class="form">
    <input
      type="text"
      name="name"
      placeholder="Enter your name"
      required
      bind:value={name}
      class="name"
    />
    <input
      type="email"
      name="email"
      placeholder="Enter your email"
      required
      bind:value={email}
      class="email"
    />
    <textarea
      name="subject"
      cols="30"
      rows="2"
      placeholder="Enter the Subject"
      required
      bind:value={subject}
      class="subject"
    />
    <textarea
      name="message"
      cols="30"
      rows="5"
      placeholder="Enter the Message"
      required
      bind:value={message}
      class="message"
    />

    <button type="submit" disabled={submitting} class="formsubmit">
      {#if submitting}
        <img src="/images/spinner.gif" class="spinner" alt="Spinner" />
      {:else}
        Send
      {/if}
    </button>
  </form>

  <div class="mediaLinks">
    <a
      href="https://www.facebook.com/naveen12309/"
      target="_blank"
      rel="noopener noreferrer"
      ><img src="assets/images/facebook.png" alt="Facebook" /></a
    >
    <a
      href="https://twitter.com/Naveen87763128"
      target="_blank"
      rel="noopener noreferrer"
      ><img src="assets/images/twitter.png" alt="Twitter" /></a
    >
    <a
      href="https://github.com/naveen0-0"
      target="_blank"
      rel="noopener noreferrer"
      ><img src="assets/images/github.png" alt="Github" /></a
    >
  </div>
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap");

  /* @ Contact Component  */
  .formTitle {
    font-size: 32px;
    text-align: center;
    padding: 25px 25px 10px;
    font-weight: bold;
    margin: 0px 0px 20px;
    color: whitesmoke;
    font-family: "Fira Code";
  }

  .form {
    width: 85%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    margin: auto;
    height: 450px;
    background-color: #222;
    padding: 20px;
    border-radius: 10px;
    position: relative;
  }

  .name,
  .email {
    outline: none;
    border: none;
    padding: 10px;
    border-radius: 5px;
    font-family: "Fira Code", monospace;
    background-color: #111;
    color: whitesmoke;
  }

  .subject,
  .message {
    outline: none;
    background-color: #111;
    border: none;
    padding: 10px;
    border-radius: 5px;
    font-family: "Fira Code", monospace;
    resize: none;
    color: whitesmoke;
  }

  .formsubmit {
    width: 100px;
    height: 40px;
    outline: none;
    border: none;
    padding: 8px 10px;
    background: linear-gradient(to right, cornflowerblue, royalblue);
    box-shadow: 3px 3px 4px #222;
    border-radius: 50px;
    color: white;
    font-family: "Fira Code", monospace;
    font-size: 16px;
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .formsubmit:active {
    box-shadow: none;
  }

  .formsubmit:hover {
    background: linear-gradient(to left, cornflowerblue, royalblue);
  }

  .mediaLinks {
    width: 85%;
    margin: auto;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 20px;
  }

  .mediaLinks img {
    width: 30px;
  }

  .spinner {
    width: 25px;
  }

  @media screen and (max-width: 450px) {
    .form {
      width: 95%;
    }
  }
</style>
