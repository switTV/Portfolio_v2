<script>
    import Hero from "../../components/home_components/Hero.svelte";
    import Button from "../../components/utils/button.svelte";

    let width_button = 470
    let text_button = "Proyectos"
    let direction_button = "/projects"
</script>

<style>
    .button_section {
        display: flex;
        justify-content: center;
    }
</style>

<!-- markup (zero or more items) goes here -->
<Hero></Hero>
<div class="button_section">
    <Button {width_button} {text_button} {direction_button}></Button>
</div>
