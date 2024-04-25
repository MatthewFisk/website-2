<style>
  #projects {
    display:block;
    max-width:1000px;
    text-align:center;
    margin:0 auto;
    margin-bottom: 1000px;
}
</style>

<script lang="ts">
  import LandingHeader from "./lib/LandingHeader.svelte";
  import SearchBar from "./lib/SearchBar.svelte";
  import ProjectCard from "./lib/ProjectCard.svelte";
  let src = "./src/assets/placeholder.webp";
</script>

<main>
  <LandingHeader />
  
  <div id='projects'>
    <h1>Projects</h1>
    <ProjectCard project_name="Falcon Racing &nbsp &nbsp Driver Interface"
                 src='./src/assets/falcon-racing-driver-interface.png'
                 tech_stack={['raspberry-pi', 'python', 'tkinter', 'sqlite']}/>
    <ProjectCard project_name="JuiceBox"
                 src='./src/assets/placeholder.webp'
                 tech_stack={['rust', 'bevy']}/>
    <ProjectCard project_name="Terrier &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp Web Front-End"
                 src='./src/assets/terrier-web-frontend.png'
                 tech_stack={['react', 'javascript', 'vite', 'html', 'css', 'figma']}/>
    <ProjectCard project_name="Mock-up &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp &nbsp System Proposal"
                 src='./src/assets/mock-up-system-proposal.jpg'
                 tech_stack={[]}/>
    <ProjectCard project_name="Orbit Simulator"
                 src='./src/assets/orbit-simulator.png'
                 tech_stack={['javascript', 'html', 'css']}/>
    <ProjectCard project_name="Courseflow Generator"
                 src='./src/assets/course-flowchart-generator.png'
                 tech_stack={['cpp']}/>
    <ProjectCard project_name="Graph Library"
                 src='./src/assets/java-graph-library.png'
                 tech_stack={['java']}/>
    <ProjectCard project_name="RC Fireboat"
                 {src}
                 tech_stack={['raspberry-pi', 'python', 'micro-python']}/>
  </div>
</main>
