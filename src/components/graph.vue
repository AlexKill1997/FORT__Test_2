<template>
    <div class="graph__content">
        <div class="graph__content__top">
            <h2 class="graph__title">Аналитика продаж</h2>
            <div class="graph__score">90</div>
        </div>
        <div class="graph__content__stat">
            <h5 class="graph__subtitle">Активных <font style="color:#6f7afb; font-weight:bold">13 проектов</font> </h5>
            <div class="month__choose">
                <svg class="calendar">
                       <use xlink:href="../assets/sprite.svg#calendar"></use>
                   </svg>
                <div class="name__month">Месяц</div>
                <transition name="fade" mode="out-in">
                    <a href="" class="link__to__month" v-if="!show" @click.prevent="show=!show">
                    <svg width="3.2rem" height="1.5rem" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
                        <polyline
                        points="0 0, 50 50, 100 0"
                        stroke="#151515"
                        stroke-width="3"
                        fill="transparent"
                        />
                    </svg>
                    </a>
                    <a href="" class="link__to__month" v-else @click.prevent="show=!show">
                    <svg width="3.2rem" height="1.5rem" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
                        <polyline
                        points="0 100, 50 25, 100 100"
                        stroke="#151515"
                        stroke-width="3"
                        fill="transparent"
                        />
                    </svg>
                    </a>
                </transition>
                <transition name="fade">
                <ul v-if="show" class="month__menu">
                    <li class="month__list" v-bind:key="item" v-for="item in items">{{ item }}</li>
                </ul>
                </transition>
            </div>
        </div>
        <div class="graph__pic">
            <img src="../assets/graph.png" class="pic" alt="">
        </div>
        <div class="graph__content__bottom">
            <div class="future__plan">
                <div class="plan__content">
                    <div class="future__color__box"></div>
                    <h6 class="meaning">Предстоящие</h6>
                </div>
            </div>
            <div class="loading__plan">
                <div class="plan__content">
                    <div class="loading__color__box"></div>
                    <h6 class="meaning">В процессе</h6>
                </div>
            </div>
            <div class="done__plan">
                <div class="plan__content">
                    <div class="done__color__box"></div>
                    <h6 class="meaning">Завершенные</h6>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
    data(){ return{
        items:[
            "Январь",
            "Февраль",
        ],
        show:false
        
        
    }
    }
}
</script>

<style lang="scss">

    .graph__content__top{
        display: flex;
    }
    .graph__content{
        width:46.9rem;
        margin-right: 2rem;
        margin-bottom: 1rem;
    }
    .graph__score{
        padding-right: 3rem;
        font-size:2.5rem
    }
    .graph__content__stat{
        display: flex;
        align-items: center;
        margin-bottom: 2.4rem;
    }
    .graph__title{
        margin-right: 13rem;
    }
    .graph__subtitle{
        margin-right: 12rem;
    }
    
    .month__choose{
        display: flex;
        align-items: flex-start;
        width: 10.6rem;
        background-color:white ;
        justify-content: space-around;
        padding: 1rem 0 1rem 1rem; 
    }

    .graph__content__bottom{
        display: flex;
    }
    .future__plan,
    .loading__plan,
    .done__plan{
        width:14.8rem;
        background-color:white ;
        margin-right:1.6rem;
        
    }

    .plan__content{
        padding: 1rem 0 0.5rem 1rem;
        display: flex;
        
    }

    .future__color__box,
    .loading__color__box,
    .done__color__box{
        width: 1rem;
        height:1rem;
        border-radius: 50%;
        margin-right: 1.6rem;
        
    }
    .loading__color__box{
        background-color: #f7b500;
    }
    .done__color__box{
        background-color: #e1e1e1;
    }
    .future__color__box{
        background-color: #6672fb;
    }
 
        .month__menu{
        align-self: flex-start;
        position: absolute;
        top:16rem;
        background-color: white;
        border: 1px solid #afcbf6;
    }
         .month__list{
        padding: 1rem;
        cursor: pointer;
        font-size: 1.3rem;
    }

    .graph__pic{
        overflow: hidden;
        width: 44.5rem;
        height: 16.4rem;
    }
    .pic{
        width: 100%;
        display: block;
    }

    .calendar{
        width: 1rem;
        height: 1rem;
    }
</style>