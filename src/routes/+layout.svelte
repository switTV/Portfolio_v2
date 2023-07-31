<script lang="ts">
    import type { LayoutData } from './$types';
    import Nav from '../components/Nav.svelte';
    
    export let data: LayoutData;
</script>

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
<div class="container">
    <div class="main-container">
        <Nav></Nav>
        <slot></slot>
    </div>
</div>