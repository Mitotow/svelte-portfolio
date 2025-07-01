<script lang="ts">
    import Navbar from "./navbar/Navbar.svelte";
    import type { NavbarLink } from "./navbar/NavbarLink";

    const links: NavbarLink[] = [
        {
            name: "Home",
            href: "/",
        },
        {
            name: "Projects",
            href: "/projects",
        },
        {
            name: "Work",
            href: "/work"
        }
    ];
</script>

<header>
    <Navbar links={links}/>
</header>

<style>
    header {
        z-index: 9999;
        position: fixed;
        left: 50%;
        bottom: var(--app-header-ymargin);
        transform: translatex(-50%);
        display: inline-flex;
    }
</style>