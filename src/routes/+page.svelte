<svelte:head>
  <title>Leiton Estrada: Personal site and portfolio</title>
</svelte:head>
<script>
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";
</script>
<h1> Leiton Leandro Estrada R.</h1>
   
<img src="images/Imagen001.jpg" alt="mike" width="200px">

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</p>
<h2>
  Latest Projects
</h2>
<div class="projects">
{#each projects.slice(0, 3) as p}
  <Project data={p} hLevel="3"/>
{/each}
</div>
