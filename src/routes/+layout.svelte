
<script>

    import { base } from "$app/paths";
    import { page } from "$app/stores";

    let pages = [
    { url: "/", title: "Home" },
    { url: "/projects", title: "Projects" },
    { url: "/contact", title: "Contact" },
    { url: "/resume", title: "Resume" },
    {url: "https://github.com/Leandr0ER/PortFolioLab5", title:"Github"}
];
</script>

<nav>
    {#each pages as p}
    <a
        href={p.url.startsWith("http") ? p.url: `${base}${p.url}`}
        class:current={$page.route.id === p.url}
        target={p.url.startsWith("http") ? "_blank" : undefined}
    >
        {p.title}
    </a>
    {/each}
</nav>

<slot /> 
