<!--
    TODO:
    Main card should scale down when expanded card increases
    Card Expanded 
-->

<script>
    export let project_name = "default";
    export let src = "./src/assets/placeholder.jpg";
    export let tech_stack = ["java", "python"];
    export let scope = 1;
    export let team_size = 1;
    export let description = "This project was fun!";
</script>

<div class="card_positioner">
    <div class="card_expand">
        <div class="card_expand_upper">
            <!-- Base Card -->
            <div class="card">
                <img {src} class="card_image" />
                <div class="blur" />
                <h2>{project_name}</h2>
                <div class="tech_stack">
                    {#each tech_stack as image_name}
                        <img src="./src/assets/{image_name}.png" />
                    {/each}
                </div>
            </div>

            <!-- Right Expansion -->
            <div class='card_expand_right'>
                <p>{description}</p>
            </div>
        </div>

        <div class="card_expand_bottom">
            <h3>Scope: {scope}</h3>
            <h3>Team Size: {team_size}</h3>
        </div>
    </div>
</div>

<style>
    /* Project Name */
    h2 {
        width: 205px; /* No wider than the image */

        position: absolute;
        transform: translateY(-100%);
        top: 195px;
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

        align-content: left;

        display: inline-block;

        border-radius: 15px;
    }

    /* Main images */
    .card_image {
        width: 215px;
        height: 215px;

        margin: 5px;

        border-top-left-radius: 15px;
        border-top-right-radius: 15px;
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

    /* Card Expansion and Position */
    .card_positioner {
        width: 225px;

        position: relative;

        display: inline-block;
        vertical-align: top;

        margin: 10px;
        margin-bottom: 335px;
    }
    .card_expand {
        background-color: #444445;

        width: 225px;

        position: absolute;
        left: -10px;
        margin: 15px;

        display: inline-block;
        vertical-align: top;
        align-content: start;

        border-radius: 15px;
        box-shadow: 0px 0px 10px 2px #2e2d2f;

        transition:
            width 0.15s ease-in-out,
            transform 0.15s ease-in-out;
    }
    .card_expand_upper {
        display: inline-flex;
    }
    .card_expand_right {
        height: 0px;

        padding: 10px;

        justify-content: center;
    }
    .card_expand_right p {
        pointer-events: none;
        opacity: 0;
        transition: opacity 0.1s ease-out;
    }
    .card_expand_bottom {
        background-color: #444445;

        height: 0px;

        border-radius: 15px;

        transition: height 0.15s ease-in-out;
    }
    .card_expand_bottom h3 {
        margin: 0px;

        opacity: 0;

        transition: opacity 0.1s ease-out;
    }

    /* Card Transitions on Hover */
    .card_expand:hover {
        width: 450px;

        transform: translateX(-25%) translateY(-25px); /* Centering the expanded card */
        z-index: 99;

        box-shadow: 0px 0px 40px 5px black;

        transition-delay: 0.3s;
    }
    .card_expand:hover .card_expand_upper {
        width: 450px;
        transition-delay: 0.3s;
    }
    .card_expand:hover .card_expand_upper .card_expand_right {
        width: 225px;
    }
    .card_expand:hover .card_expand_upper .card_expand_right p {
        opacity: 1;
        transition: opacity 0.45s ease-in;
        transition-delay: 0.3s;
    }
    .card_expand:hover .card_expand_bottom {
        height: 100px;
        transition-delay: 0.3s;
    }
    .card_expand:hover .card_expand_bottom h3 {
        opacity: 1;
        transition: opacity 0.45s ease-in;
        transition-delay: 0.3s;
    }
    .card_expand:hover .card img {
        border-top-right-radius: 0px;
        transition-delay: 0.3s;
    }
    .card_expand:hover .card {
        /*transform: scale(0.7);*/
        animation: lighten 0.35s 1;
        animation-timing-function: steps(1, end);
    }
    @keyframes lighten {
        0% {
            background-color: #6a686d;
        }
        100% {
            background-color: #444445;
        }
    }
</style>
