<script>
import Nav from "$lib/nav.svelte";
import Title from "$lib/title.svelte";
import '../styles/global.css';
</script>

<header>
    <Nav />
    <Title title="Main Page Title" />
</header>
<main>
    <!-- page content -->
    <slot></slot>
</main>
<footer>
    <p>Copyright 2022 My Svelte App</p>
</footer>

<style>
    header {
        display: flex;
        justify-content: center;
    }
    main {
        max-width: 960px;
        margin: 20px auto;
    }
    footer {
        text-align: center;
    }
</style>