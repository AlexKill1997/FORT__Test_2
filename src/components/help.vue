<template>
    <div class="help__container">
        <div class="picture">
            <img src="../assets/help.png" alt="" class="pic">
        </div>
        <div class="help__content">
            <h6 class="help__title">Нужна помощь?</h6>
            <p class="help__text">Есть ли у вас проблемы при использовании программы?</p>
        </div>
        <div class="btn btn-primary">Пишите нам</div>
    </div>
</template>

<style lang="scss">
    .help__container{
        width: 32.5rem;
        background-color: white;
        padding: 0.5rem 0 1rem 2.2rem;
    }
    .picture{
        height: 15.7rem;
        width: 26.8rem;
        margin-bottom: 1rem;
    }
    .pic{
        display:block;
        width: 100%;
    }
    .help__content{
        width:15.4rem
    }
    .help__title{
        font-size: 1.4rem;
    }

    .help__text{
        font-size: 1rem;
        margin-bottom: 2.7rem;
    }
    .btn-primary{
        width: 13.5rem;
        font-size: 1rem;
    }

</style>