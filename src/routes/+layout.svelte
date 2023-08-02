<script lang="ts">
    import type { LayoutData } from "./$types";
    import { fade } from "svelte/transition";
    import Nav from "../components/utils/Nav.svelte";

    export let data: LayoutData;
</script>

<div class="container">
    <div class="main-container">
        <Nav />

        <main>
            {#key data.url}
                <div in:fade={{duration: 200}}>
                    <slot />
                </div>
            {/key}
        </main>
    </div>
</div>

<style>
    :global(*) {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .container {
        width: 100vw;
        display: flex;
        justify-content: center;
    }

    .main-container {
        width: 80vw;
    }
</style>
