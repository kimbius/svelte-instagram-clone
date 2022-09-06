<script>
    import "../app.css";

    import MainNavbar from "../components/MainNavbar.svelte";

    export const ssr = false;
</script>

<MainNavbar />

<div class="min-h-screen">
    <slot />
</div>
