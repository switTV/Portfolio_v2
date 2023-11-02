<script>
    // import { IconMenu, IconX } from "@tabler/icons-svelte";

    let menu_state = true

    function change_menu_state() {
        menu_state = !menu_state
    }
</script>

<style>
    .deactivated{
        display: none;
    }

    .Bars_menu_options {

        flex-direction: column;
        height: 200px;
        width: 100%;
        z-index: 2;
        
        
        
        position: absolute;
        
        right: 0px;
    }

    .Bars_menu svg {
        color: #1282A2;
    }
    
    .Bars_menu_options a{
        background-color: #fff;
        height: 33%;
        display: flex;
        align-items: center;
        text-decoration: none;
        padding-left: 10%;
        color: #001F54;

        font-family: Montserrat, sans-serif;
        
        border-bottom: 2px solid #2366da;
    }

    .Bars_menu_options a:nth-child(1) {
        margin-top: 20px;
    }
</style>

<!-- al tocar el boton de las barras debe de aparecer un menu voladizo -->

<!-- markup (zero or more items) goes here -->
<div class="Bars_menu">
    <div class="container_icon" on:click={change_menu_state}>
        {#if menu_state}
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-menu" width="32" height="32" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
            <path d="M4 8l16 0"></path>
            <path d="M4 16l16 0"></path>
            </svg>
        {:else}
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-x" width="32" height="32" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
            <path d="M18 6l-12 12"></path>
            <path d="M6 6l12 12"></path>
            </svg>
        {/if}
    </div>
    <div class="Bars_menu_options" class:deactivated={menu_state} class:activated={!menu_state}>
        <a href="/home">About Me</a>
        <a href="/projects">Proyectos</a>
        <a href="/contact">Contacto</a>
    </div>
    <div class="overlay"></div>
</div>