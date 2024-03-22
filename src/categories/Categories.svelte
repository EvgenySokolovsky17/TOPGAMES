<script>
    let categories = [
        { id: "Easy", name: "Easy" },
        { id: "Normal", name: "Normal" },
        { id: "Hard", name: "Hard" },

    ];
</script>


<div class="h-stack">
    <input class="text" placeholder="Введите категорию"/>
    <button>Добавить категорию</button>
</div>
<div class="v-stack">
    <div>Список категорий</div>
</div>

{#each categories as category}
    <div class="card-category">
        <b>{category.name}</b>
        <div class="status"></div>
        <a href={`/categories/${category.id}`} class="button-link">Перейти в категории</a>
    </div>
{/each}


