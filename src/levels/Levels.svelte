<script>

    import lev from '$lib/images/lev.svg';
    import LevelsCard from "./LevelsCard.svelte";



    let levels = [
        { name: 'В чем сила брат?', answer: 'В правде!'},
        { name: 'В чем сила брат?', answer: 'В правде!'},
        { name: 'В чем сила брат?', answer: 'В правде!'},
        { name: 'В чем сила брат?', answer: 'В правде!'},
        { name: 'В чем сила брат?', answer: 'В правде!'},




    ];

</script>
<LevelsCard />

{#each levels as level}
<div class="h-stack">
    <div class="v-stack">
        <div class="v-stack-img">
            <img src={lev} alt="Icon" class="v-stack-img"/>
            <svg width="110" height="70" viewBox="0 0 100 100">
        </div>
    </div>
    <div class="text-column">
        <div class="text-right">{level.name}</div>
        <div class="divider"></div>

        <div class="text-right">{level.answer}</div>
    </div>
</div>
{/each}











<style>
    body {
        font-family: Arial, sans-serif;
        margin: 20px;

    }
    .h-stack {
        background-color: #2128bd;
        border: 1px solid #ccc;
        border-radius: 5px;
        padding: 10px;
        margin-bottom: 10px;
        display: flex;
        flex-direction: row;
        justify-content: space-between; /* Изменил на space-between для равномерного распределения элементов */
    }

    .v-stack {
        /*display: flex;*/
        /*flex-direction: row;*/
    }
    .v-stack-img {
        margin-left: 0px;
        margin-top: 13px;
    }

    .text-column {
        display: flex;
        flex-direction: column; /* Расположение текста в столбик */
        align-items: center; /* Размещение элементов по центру */
        margin-left: 90px;
    }

    .divider {
        height: 1px;
        background-color: #ccc;
        margin: 5px 0;
        width: 100%; /* Добавлено */
        align-self: center; /* Добавлено */
    }

    .text-right{
        margin: 15px;
        color: white;
    }




</style>