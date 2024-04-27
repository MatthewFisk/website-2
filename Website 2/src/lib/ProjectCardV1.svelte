<script>
    export let project_name = "default";
    export let src = "./src/assets/placeholder.jpg";
    export let tech_stack = ["java", "python"];
    export let scope = 1;
    export let team_size = 1;
</script>

    <div class="card">

        <!-- Base Card -->
        <img {src} class="card_image" />
        <div class="blur" />
        <h2>{project_name}</h2>
        <div class="tech_stack">
            {#each tech_stack as image_name}
                <img src="./src/assets/{image_name}.png" />
            {/each}
        </div>

        <!-- Expanded Card (Hidden by Default) -->
        <div class='card_expanded'>
        <img {src} class='expanded_card_image'/>
        <div class='tech_stack'>
            {#each tech_stack as image_name}
                <img src='./src/assets/{image_name}.png'>
            {/each}
        </div>
        <h3>Scope: {scope}</h3>
        <p>Team Size: {team_size}</p>
    </div>

    </div>

<style>
    /* Project Name */
    h2 {
        width: 205px; /* No wider than the image */

        position: absolute;
        transform: translateY(-100%); 
        top: 200px;
        left: 15px;

        text-wrap: wrap;
        text-align: left;

        user-select: none;
    }

    /* Card, Expanded Version, and Hover Function */
    .card {
        background-color: #444445;

        width: 225px;
        height: 285px;
        margin: 10px;

        position: relative;

        display: inline-block;
        vertical-align: top;

        border-radius: 15px;
        box-shadow: 0px 0px 10px 2px #2e2d2f;
    }
    .card:hover {
        background-color: #6a686d;
    }
    .card_expanded {
        background-color: #444445;

        position: relative;
        right: 112.5px;
        bottom: 295px;
        z-index: 99;

        overflow: hidden;

        border-radius: 15px;
        box-shadow: 0px 0px 40px 5px black;

        /* height, overflow, scale make it invisible before hover. */
        height: 0px;
        overflow: hidden;
        transform: scale(0);
        transform-origin: center 120px;
        transition: transform 0.15s ease-in-out;
    }
    .card:hover .card_expanded {
        width: 450px; /* Width and height unaffected by transition time. */
        height: 350px;

        transform: scale(
            1
        ); /* Transition from scale(0) -> scale(1) makes .card_expanded pop out from the .card. */
        transition-delay: 0.3s; /* Gives some delay when the user hovers over the card before popping out the expanded view so we're sure the user really wants to see it. */
    }

    /* Main images */
    .card_image {
        width: 215px;
        height: 215px;

        margin: 5px;

        border-top-left-radius: 15px;
        border-top-right-radius: 15px;
    }
    .expanded_card_image {
        width: 175px;
        height: 175px;
        margin: 10px;

        position: relative;
        top: 0px;
        left: 0px;

        display: block;

        border-top-left-radius: 15px;
        align-items: start;
    }
    .blur {
        background: rgba(0, 0, 0, 0)
            linear-gradient(
                to bottom,
                rgba(0, 0, 0, 0) 10%,
                rgba(0, 0, 0, 0.1) 40%,
                rgba(0, 0, 0, 0.5) 65%,
                rgba(0, 0, 0, 1) 100%
            );

        width: 215px;
        height: 200px;

        position: absolute;
        top: 20px;
        left: 5px;
        vertical-align: top;
    }

    /* Tech Stack */
    .tech_stack {
        height: 35px; /* Ensures that .tech_stack takes up room even if there are no images */
        margin-top: 5px;
        padding-left: 10px;
        display: block;
        text-align: left;
    }
    .tech_stack img {
        height: 35px;

        margin-right: 5px;

        /* White border */
        -webkit-filter: drop-shadow(1px 1px 0 white)
            drop-shadow(-1px 1px 0 white) drop-shadow(1px -1px 0 white)
            drop-shadow(-1px -1px 0 white);
        filter: drop-shadow(1px 1px 0 white) drop-shadow(-1px 1px 0 white)
            drop-shadow(1px -1px 0 white) drop-shadow(-1px -1px 0 white);
    }

    .foo {
        background-color: red;

        height: 0px;

        transition: height 0.15s ease-in-out;
    }

    .card_parent {
        margin: 15px;

        border: solid green 10px;

        position: relative;

        display: inline-block;
        vertical-align: top;
    }

    .card_parent:hover .foo{
        height: 100px;
    }

    .card_parent:hover .foo h3 {
        opacity: 1;
    }

    .foo h3 {
        margin: 0px;
        opacity: 0;
        transition: opacity 0.3s ease-in;
    }
</style>
