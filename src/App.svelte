<script>
  import Router from "svelte-spa-router";
  import NavBar from "./components/NavBar.svelte";
  import Home from "./components/Home.svelte";
  import About from "./components/About.svelte";
  import Skills from "./components/Skills.svelte";
  import Projects from "./components/Projects.svelte";
  import Contact from "./components/Contact.svelte";
  const routes = {
    "/": Home,
    "/about": About,
    "/skills": Skills,
    "/projects": Projects,
    "/contact": Contact,
  };
</script>

<main>
  <NavBar />
  <Router {routes} />
</main>

<style>
</style>
