<script lang="ts">
    import img_hero from "../../assets/img-hero.png"

    let mouseX = 0
    let mouseY = 0

    function handleMouseMove(event:any) {
        mouseX = event.clientX
        mouseY = event.clientY
    }
</script>

<style>
    .Hero {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 70vh;
    }

    .Hero .Hero-left-section .Hero-left-section-text h2{
        font-family: "Montserrat";
        color: #1768AC;
        font-size: 64px;
        margin-bottom: 0;
    }
    
    .Hero .Hero-left-section .Hero-left-section-text p{
        font-family: "Montserrat";
        color: #1768AC;
        font-size: 20px;
    }

    .Hero .Hero-right-section .Hero-left-section-img {
        position: relative;
    }

    .Hero .Hero-right-section .Hero-left-section-img .Hero-img {
        width: 300px;
        height: 300px;
        border-radius: 5px;
    }
    .Hero .Hero-right-section .Hero-left-section-img .Hero-img-bg {
        width: 300px;
        height: 300px;
        background-color: #1768AC;
        border-radius: 5px;
        position: absolute;
        z-index: -1;
        top: 20px;
        left: 20px;
        bottom: 20px;
    }
</style>

<!-- markup (zero or more items) goes here -->

<div class="Hero" on:mousemove={handleMouseMove}>
    <div class="Hero-left-section">
        <div class="Hero-left-section-text">
            <h2>Máximo</h2>
            <p>Desarrollador Frontend</p>
        </div>
    </div>
    <div class="Hero-right-section">
        <div class="Hero-left-section-img">
            <div class="Hero-img" style="background-image: url({img_hero}); transform: translate({mouseX / 50}px, {mouseY / 50}px);"></div>
            <div class="Hero-img-bg" style="transform: translate({mouseX / 30}px, {mouseY / 30}px);">i</div>
        </div>
    </div>
</div>