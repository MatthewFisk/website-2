<script>
    export let words = "default";
    export let href = "https://www.google.com"
</script>

<style>
    .button {
        background-color: #6a686d;

        border-radius: 40px;

        display: inline-block;

        margin-left: 2px;

        height: 45px;
        width: 135px;
    }
    .button:hover {
        animation: lighten 0.35s 1;
        animation-fill-mode: forwards;
    }
    @keyframes lighten {
        0% {
            background-color: #6a686d;
        }
        100% {
            background-color: #a9a7ac; /* #a9a7ac */
        }
    }

    .button h3 {
        margin-top: 6px;
        pointer-events: none;
    }
    a {
        color: white;
    }
</style>

{#if href != "none"}
    <a href={href}>
        <div class="button">
            <h3>{words}</h3>
        </div>
    </a>
{/if}