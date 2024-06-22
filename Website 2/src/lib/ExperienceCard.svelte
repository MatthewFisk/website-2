<script>
    export let company = "default";
    export let location = "default";
    export let role = "default";
    export let dates = "default";
    export let description = "default";
    export let image = "./src/assets/placeholder.webp";
</script>

<style>
    .background {
        background-color: #444445;
        width: 55%;
        margin: 30px auto;
        display: flex;
        border-radius: 20px;
    }
    .background .description {
        position: relative;
        display: inline-block;
    }
    img {
        width: 150px;
        height: 150px;
        margin: 15px;
        position: relative;
        display: inline;
        filter: drop-shadow(1px 1px 0 white) drop-shadow(-1px 1px 0 white)
            drop-shadow(1px -1px 0 white) drop-shadow(-1px -1px 0 white);
    }
    h2 {
        margin: 0px;
        margin-top: 10px;
        position: relative;
        left: 15px;
        text-align: left;
    }
    h3 {
        margin: 0px;
        position: relative;
        left: 15px;
        text-align: left;
        font-weight: 500;
    }
    .location {
        position: absolute;
        right: 30px;
        text-align: right;
        margin-top: 17px;
    }
    p {
        max-width: 90%;
        margin: 0px;
        margin-top: 15px;
        margin-bottom: 10px;
        position: relative;
        left: 15px;
        text-align: left;
    }

</style>

<div class="background">
    <img src={image}/>
    <div class="description">
        <h3 class="location">{location}</h3>
        <h2>{company}</h2>
        <h3>{role}</h3>
        <h3>{dates}</h3>
        <p>{description}</p>
    </div>
</div>