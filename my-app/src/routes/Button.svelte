<script>
    const CatNameAndBreed = ['catName', 'breed'];
 let data = {
    catData: undefined,
    loading: false,
 };
 /* let CatNameAndBreed; */
    async function LoadData() {
        data.loading = true;
        const response = await fetch('/random-cat')
        const CatNameAndBreed = await response.json();
        data = {
            catData: CatNameAndBreed,
            loading: false,
        };
    }
    console.log(CatNameAndBreed) 
</script>

<button on:click={LoadData}>Generate Breed and Name!</button>
{#if data.loading === true}
loading cat name and breed...
{:else if data.catData != undefined}
    {data.catData}
    {/if}
<style>
    button{
        color: white;
        background-color: black;
        height: 50px;
        width: 250px;
        font-size: 1rem;
        padding: 10px;
    }
    button:hover {
        cursor: pointer;
        color: black;
        background-color: white;
        box-shadow: 3px 3px 0px 3px rgba(0, 0, 0, 0.75);
       transition: ease-in 300ms;
    }
</style>