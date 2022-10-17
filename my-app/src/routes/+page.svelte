<script>
import Button from "./Button.svelte"
import { onMount } from "svelte";

</script>
    
    <body>
        <main>
        <div class="generator">
            <h2>Cat name and breed generator</h2>
            <Button result="any"></Button>
            </div>
            </main>

    </body>


<style>
    :global(*) {
        box-sizing: border-box;
        margin: 0;
        padding: 0%;
    }
    main {
        height: 100vh;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .generator {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        height: 20%;
        width: 30%;
        background-color: gainsboro;
    }
    h2 {
        text-align: center;
        font-size: 2rem;
    }
</style>