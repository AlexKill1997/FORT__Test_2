<template>
    <div class="side__container">
        <div class="side__logo">
            <img alt="logo" src="../assets/logo_new.png" class="logo"/>
        </div>
        <div class="side__line"></div>
        <h6 class="side__title">Меню</h6>
        <ul class="side__menu">
            <li class="panel" :class="{active : activeLink === 1}">
               <div  @click="activeLink = 1" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#panel"></use>
                   </svg>
                    <p class="content__text">Панель</p>
                    <div v-if="activeLink === 1" class="content__score"><p class="score">4</p></div>
               </div>
            </li>
            <li class="panel" :class="{active : activeLink === 2}">
               <div  @click="activeLink = 2" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#user"></use>
                   </svg>
                    <p class="content__text">Расширения</p>
                    <div v-if="activeLink === 2" class="content__score"><p class="score">3</p></div>
               </div>
               </li>
            <li class="panel" :class="{active : activeLink === 3}">
               <div  @click="activeLink = 3" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#content"></use>
                   </svg>
                    <p class="content__text">Дизайн</p>
                    <div  v-if="activeLink === 3" class="content__score"><p class="score">2</p></div>
               </div>
               </li>
            <li class="panel" :class="{active : activeLink === 4}">
               <div  @click="activeLink = 4" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#chat"></use>
                   </svg>
                    <p class="content__text">Продажи</p>
                    <div v-if="activeLink === 4" class="content__score"><p class="score">1</p></div>
               </div>
               </li>
            <li class="panel" :class="{active : activeLink === 5}">
               <div  @click="activeLink = 5" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#baggage"></use>
                   </svg>
                    <p class="content__text">Покупатели</p>
                    <div v-if="activeLink === 5" class="content__score"><p class="score">7</p></div>
               </div>
               </li>
            <li class="panel" :class="{active : activeLink === 6}">
               <div  @click="activeLink = 6" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#month"></use>
                   </svg>
                    <p class="content__text">Маркетинг</p>
                    <div v-if="activeLink === 6" class="content__score"><p class="score">10</p></div>
               </div>
               </li>
            <li class="panel" :class="{active : activeLink === 7}">
               <div  @click="activeLink = 7" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#window"></use>
                   </svg>
                    <p class="content__text">Система</p>
                    <div  v-if="activeLink === 7" class="content__score"><p class="score">11</p></div>
               </div>
               </li>
        </ul>
        <h6 class="side__title">Поддержка</h6>
        <ul class="side__support">
            <li class="panel" :class="{active : activeLink === 8}">
               <div  @click="activeLink = 8" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#question"></use>
                   </svg>
                    <p class="content__text">Нужна помощь?</p>
                    <div v-if="activeLink === 8" class="content__score"><p class="score">6</p></div>
               </div>

               </li>
            <li class="panel" :class="{active : activeLink === 9}">
               <div  @click="activeLink = 9" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#contact"></use>
                   </svg>
                    <p class="content__text">Контакты</p>
                    <div v-if="activeLink === 9" class="content__score"><p class="score">6</p></div>
               </div>
               </li>
        </ul>
        <h6 class="side__title">Settings</h6>
        <ul class="side__settings">
            <li class="panel" :class="{active : activeLink === 10}">
               <div  @click="activeLink = 10" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#setting"></use>
                   </svg>
                    <p class="content__text">Настройки</p>
                    <div v-if="activeLink === 10" class="content__score"><p class="score">6</p></div>
               </div>

               </li>
           <li class="panel" :class="{active : activeLink === 11}">
               <div  @click="activeLink = 11" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#moon"></use>
                   </svg>
                    <p class="content__text">Темы</p>
                    <div v-if="activeLink === 11" class="content__score"><p class="score">6</p></div>
               </div>

               </li>
            <li class="panel" :class="{active : activeLink === 12}">
               <div  @click="activeLink = 12" class="panel__content">
                   <svg class="icon">
                       <use xlink:href="../assets/sprite.svg#exit"></use>
                   </svg>
                    <p class="content__text">Выйти</p>
                    <div v-if="activeLink === 12" class="content__score"><p class="score">6</p></div>
               </div>

               </li>
        </ul>

        
    </div>
</template>

<script>
export default {
    data(){ return{
        changed:false,
        activeLink:undefined,
        show:false
    }
    },
    methods:{
        setupActive(){
            this.changed=!this.changed
        }
    }
}
</script>

<style lang="scss">
    .side__container{
        display:flex;
        flex-direction: column;
        align-items: center;
        max-width: 100%;
        margin-top: 2.5rem;
       
    }
    .side__logo{
        width: 13rem;
        height: 7.7rem;
        margin-bottom: 3.4rem;
        
    }

    .logo{
        max-width:100%;
        display: block;
    }
    .side__line{
        width: 100%;
        height:1px;
        background-color: #323e4a;
        margin-bottom: 4.4rem;
    }

    .side__title{
        align-self: flex-start;
         padding-left:10%;
         color: #7c8591;
         text-transform: uppercase;
         margin-bottom: 3rem;
    }

    

    .panel:last-child{
        margin-bottom: 0;
    }
    .side__menu{
        margin-bottom: 16rem;
        align-self: flex-start;
        padding-left:10%;
    }
    .icon{
        width: 1.5rem;
        height: 1.5rem;
        fill:#e3e4e5;
        margin-right: 1.5rem;
    }
    .panel__content{
        display: flex;
        padding:1rem 1rem 0 1rem;
        color: #e3e4e5;
        font-size: 1.5rem;
        cursor: pointer;

    }
    .content__text{
        margin-right: 1.5rem;
    }


    .side__settings{
        align-self: flex-start;
        padding-left:10%;
    }
    .side__support{
        align-self: flex-start;
        padding-left:10%;
        margin-bottom: 3.9rem;
    }
    .active{
        background-color: #576774;
        border-radius: 7%;
    }

    .content__score{
        width:2rem;
        height: 2rem;
        border-radius: 50%;
        background-color: white;
        display: flex;
        justify-content: center;
    }

    .score{
        color:#a1a8eb;
        font-size:1rem
    }

</style>