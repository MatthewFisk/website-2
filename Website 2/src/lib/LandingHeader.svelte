<style>
    .background {
        background-color: #6a686d;
    }
    .landing_header {
        height: 400px;
        margin: 0px auto;
        width: 80%;
        display: flex;
        background-color: #6a686d;
        border-bottom: solid 2px white;
    }
    .left {
        flex: 2 0 0;
        padding-left:75px;
        padding-right: 75px;
        text-align: left;
    }
    .right {
        flex: 1 0 0;
        padding-left:50px;
        padding-right: 50px;
    }
    .profile_picture {
        width: 300px;
        margin-top: 50px;
        animation: bob 2.5s;
        animation-iteration-count: infinite;
        animation-timing-function: ease;

        border-radius: 125px;

        box-shadow: 0px 0px 40px 5px black;
    }
    .links {
        background-color: #6a686d;
        width: 45%;
        margin: 0 auto;
        padding-top: 25px;
        padding-bottom: 25px;
        display: flex;
    }
    .links a {
        margin: auto;
        display: flex;
    }
    .links a h2 {
        color: white;
        border-bottom: 2.5px solid white;
        display: inline-block;
        line-height: 1.10;
    }
    .links a img {
        width: 30px;
        height: 30px;
        margin: auto;
        margin-right: 10px;
    }
    @keyframes bob {
        0% {
            margin-top: 45px;
        }
        50% {
            margin-top: 55px;
        }
        100% {
            margin-top: 45px;
        }
    }
</style>

<div class="background">
    <div class='landing_header'>
        <div class="left">
            <img>
            <h1>Matthew Fisk</h1>
            <h2>I'm a freshly graduated Computer Science major from Seattle Pacific University.
                I have some experience in both front-end and back-end development.
                Currently looking for work.</h2>
            <h2>Reach out if you'd like to know more!</h2>
        </div>
        <div class="right">
            <img src="./src/assets/profile-picture.jpg" class="profile_picture"/>
        </div>
    </div>
    <div class="links">
        <a href="https://github.com/mahttchoo">
            <img src="./src/assets/github.png">
            <h2>GitHub</h2>
        </a>
        <a href="mailto:matthewfisktkd@gmail.com">
            <img src="./src/assets/email.png">
            <h2>Email</h2>
        </a>
        <a href="https://www.linkedin.com/in/matthew-fisk-046a53250/">
            <img src="./src/assets/linkedin.png">
            <h2>LinkedIn</h2>
        </a>
        <a href="./Matthew Fisk Resume 2024.pdf">
            <img src="./src/assets/resume.png">
            <h2>Resume</h2>
        </a>
    </div>
</div>