<script lang="ts">
	import type { NavbarLink } from "./NavbarLink";

	let props: { links: NavbarLink[] } = $props();
</script>

<nav class="app__navbar">
	{#each props.links as link (link.href)}
		<a class="app__navbar__link" href={link.href}>{link.name}</a>
	{/each}
</nav>

<style>
	.app__navbar {
		position: relative;
		display: flex;
		width: 30vw;
		box-shadow:
			rgba(0, 0, 0, 0.4) 0px 2px 4px,
			rgba(0, 0, 0, 0.3) 0px 7px 13px -3px,
			rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
		border-radius: var(--app-nav-borderradius);
	}

	.app__navbar__link {
		flex: 1;
		text-decoration: none;
		color: black;
		padding: 0.5em 1em;
		font-size: var(--app-nav-font-size);
		text-align: center;
		box-sizing: border-box;
		transition: cubic-bezier(0.6, -0.28, 0.735, 0.045) 0.2s background;
	}

	.app__navbar__link:hover {
		background-color: rgba(0, 0, 0, 0.2);
	}

	.app__navbar > :first-child {
		border-radius: var(--app-nav-borderradius) 0 0 var(--app-nav-borderradius);
	}

	.app__navbar > :last-child {
		border-radius: 0 var(--app-nav-borderradius) var(--app-nav-borderradius) 0;
	}
</style>
