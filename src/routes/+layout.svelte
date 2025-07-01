<script lang="ts">
    import "../app.css";
    import Header from "$lib/components/header/header/Header.svelte";
</script>

<Header />

<main>
    <slot></slot>
</main>