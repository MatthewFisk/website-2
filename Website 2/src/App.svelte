<style>
  .projects {
    display:block;
    max-width:1200px;
    margin:0 auto;
    margin-top: 50px;
}
</style>

<script lang="ts">
  import LandingHeader from "./lib/LandingHeader.svelte";
  import SearchBar from "./lib/SearchBar.svelte";
  import ProjectCard from "./lib/ProjectCard.svelte";
  import ProjectCardV1 from "./lib/ProjectCardV1.svelte";
  import Experience from "./lib/Experience.svelte";
  import Skills from "./lib/Skills.svelte";
  import Contact from "./lib/Contact.svelte";
  let src = "./src/assets/placeholder.webp";
</script>

<main>
  <LandingHeader />
  <div class='projects'>
    <h1>Projects</h1>
    <ProjectCard project_name="Falcon Racing &nbsp &nbsp Driver Interface"
                 src='./src/assets/falcon-racing-driver-interface.png'
                 tech_stack={['raspberry-pi', 'python', 'tkinter', 'sqlite']}
                 scope={4}
                 team_size={3}
                 date='Fall 2022 - Spring 2023'
                 description="Was a member of an automotive engineering club. Used a
                              Raspberry Pi 4 to hook up several sensors to the car, displaying
                              the current gear, speed, and current fuel levels."
                 learn_more='/dashboard'
                 source_code='https://github.com/mclemmer7/Driver-Interface/tree/main'/>
    <ProjectCard project_name="JuiceBox"
                 src='./src/assets/juicebox.png'
                 tech_stack={['rust', 'bevy']}
                 scope={4}
                 team_size={4}
                 date='Fall 2023 - Spring 2024'
                 description="Real-time 2D fluid simulation. Senior software engineering
                              project."
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='https://github.com/Aeronautical-Axolotls/JuiceBox'/>
    <ProjectCard project_name="Terrier &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp Web Front-End"
                 src='./src/assets/terrier-web-frontend.png'
                 tech_stack={['react', 'javascript', 'vite', 'html', 'css', 'figma']}
                 scope={3}
                 team_size={1}
                 date='Summer 2023'
                 description='Internship project for Wet Dog Weather. Built them a web
                              frontend for their "Terrier" weather graphics tool.'
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='none'/>
    <ProjectCard project_name="Mock-up &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp System Proposal"
                 src='./src/assets/mock-up-system-proposal.jpg'
                 tech_stack={[]}
                 scope={2}
                 team_size={1}
                 date='Fall 2022'
                 description="Mock-up technical document for a hypothetical proposed software
                              product. Written for my System Design Class."
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='none'/>
    <ProjectCard project_name="Orbit Simulator"
                 src='./src/assets/orbit-simulator.png'
                 tech_stack={['javascript', 'html', 'css']}
                 scope={1}
                 team_size={1}
                 date='Fall 2022'
                 description="Orbital Simulation that runs in the browser. Made for fun."
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='https://github.com/Aeronautical-Axolotls/JuiceBox'/>
    <ProjectCard project_name="Courseflow Generator"
                 src='./src/assets/course-flowchart-generator.png'
                 tech_stack={['cpp']}
                 scope={2}
                 team_size={2}
                 date='Winter 2023'
                 description="Uses graph theory to construct an optimal course sequence given
                              a list of required courses. Final project for my Algorithm Design
                              and Analysis class."
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='https://github.com/mahttchoo/Courseflow-Flowchart-Generator'/>
    <ProjectCard project_name="Graph Library"
                 src='./src/assets/java-graph-library.png'
                 tech_stack={['java']}
                 scope={1}
                 team_size={1}
                 date='Winter 2023'
                 description="Graph data structure library. Implements basic use cases like
                              vertices, undirected edges, directed edges, and edge weights
                              as well as some common search algorithms. Made as a self-study."
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='https://github.com/mahttchoo/Java-Graph-Library'/>
    <ProjectCard project_name="RC Fireboat"
                 src='./src/assets/rc-fireboat.png'
                 tech_stack={['raspberry-pi', 'python', 'micro-python']}
                 scope={2}
                 team_size={4}
                 date='Spring 2024'
                 description="Used a Raspberry Pi Pico H to build a remote controlled fireboat.
                              It uses Wifi and is able to go forwards, backwards, steer, and
                              shoot a water cannon. Made for my Microcontroller System Design class."
                 learn_more='https://aeronautical-axolotls.github.io/JuiceBoxSite.github.io/'
                 source_code='https://github.com/Aeronautical-Axolotls/JuiceBox'/>
  </div>
  <Experience />
  <Skills />
  <Contact />
</main>
