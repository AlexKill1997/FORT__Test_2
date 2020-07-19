<template>
    <div class="container__top">
        <div class="field__choose" href="link__user">
            <transition name="fade" mode="out-in">
                <a href="" class="link__to__user menu" v-if="!show" @click.prevent="show=!show">
                    <svg width="3.2rem" height="1.5rem" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
                        <polyline
                        points="0 0, 50 50, 100 0"
                        stroke="#151515"
                        stroke-width="3"
                        fill="transparent"
                        />
                    </svg>
                </a>
                <a href="" class="link__to__user clear" v-else @click.prevent="show=!show">
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
                <ul v-if="show" class="user__menu">
                    <li class="user__list" v-bind:key="item" v-for="item in items">{{ item }}</li>
                </ul>
            </transition>
            <h3 class="field__choose__title">John Doe</h3>
            <div class="online"></div>
        </div>
    </div>
</template>

<script>
export default {
    
    data(){ return{
        items:[
            "Adam Smith",
            "George Washington",
        ],
        show:false
        
        
    }
    }
}
</script>

<style lang="scss">
    .container__top{
        height: 6rem;
        display: flex;
        align-items: center;
        justify-content: flex-end;
        
    }

    .field__choose{
        display: flex;
        align-items: center;
    }

    .field__choose__title{
        margin-right: 1.6rem;
    }

    .online{
        background-color: #afcbf6;
        height:3.6rem;
        width: 3.6rem;
        margin-right:2rem;
        border-radius: 50%;
        overflow: hidden;
    }

    .user__menu{
        align-self: flex-start;
        position: absolute;
        top: 4rem;
        right:3.5rem;
        background-color: white;
        border: 1px solid #afcbf6;
    }
    .user__list{
        padding: 1rem;
        cursor: pointer;
        font-size: 1.3rem;
    }
  
</style>