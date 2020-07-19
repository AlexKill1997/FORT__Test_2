<template>
    <ul class="statistics__content">
        <li class="square">
            <div class="square__content">
                <h3 class="square__title">Заказы</h3>
                <p class="thousand">1.7К</p>
                <p class="more">Подробнее</p>
            </div>
        </li>
        <li class="square">
            <h3 class="square__title">Распродажа</h3>
                <p class="thousand">24.2К</p>
                <p class="more">Подробнее</p>
        </li>
        <li class="square">
            <h3 class="square__title">Онлайн</h3>
                <p class="thousand">17.7К</p>
                <p class="more">Подробнее</p>
        </li>
        <li class="square">
            <h3 class="square__title">Общие</h3>
                <p class="thousand">43.6К</p>
                <p class="more">Подробнее</p>
        </li>
    </ul>
</template>

<style lang="scss">
    .statistics__content{
        display: flex;
        flex-wrap: wrap;
        color: white;
        width: 40rem;
    }
    .square{
        width:18rem;
        background-color:#7faaf8 ;
        border-radius: 10%;
        margin-right:1.5rem;
        padding: 2rem 0 2rem 1rem;
        margin-bottom: 2rem;
    }
    .square__title{
        margin-bottom: 1.5rem;
        font-size: 3rem;
    }
    .thousand{
        font-size: 3rem;
    }
    .more{
        font-size: 1.4rem;
    }
</style>