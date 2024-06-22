<script>
    import ExperienceCard from "./ExperienceCard.svelte";

</script>
<style>
    .background {
        margin-top: 100px;
    }
</style>

<div class='background'>
    <h1>Experience</h1>
    <ExperienceCard company="Team Aeronautical Axolotls"
                    location="Seattle, WA"
                    role="Software Engineer, Assistant Scrummaster"
                    dates="September 2023 - June 2024"
                    image="./src/assets/aeronautical-axolotls.png"
                    description='Worked with a team of 4 other students to build JuiceBox, a 2D fluid simulator, over a
                                 year long course sequence at Seattle Pacific University. Written entirely in Rust using
                                 the Bevy game engine, see "Projects" above for more information.'/>
    <ExperienceCard company="Wet Dog Weather"
                    location="Remote"
                    role="Software Development Intern"
                    dates="Summer 2023"
                    image="./src/assets/wet-dog-weather.png"
                    description='Sole intern at Wet Dog Weather. Built a front-end for their web port of their "Terrier"
                                 weather graphics interface. Used React and Vite, see "Projects" above for more information.'/>
</div>