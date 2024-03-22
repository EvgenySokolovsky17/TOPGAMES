<script>
    export let data;

    let categories = [
        { id: "1", level: "One" },
        { id: "2", level: "Two" },
        { id: "3", level: "Three" },

    ];
</script>

<h1>{data.id}</h1>

{#each categories as category}
    <button>{category.level} </button>
{/each}


