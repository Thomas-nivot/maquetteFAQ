<template>

    <div v-bind:class="{grey:isClicked, lightgrey: !isClicked}" class="mb-5 py-4 md:py-8 px-5 md:px-10 flex transition-colors duration-300" >
        <div class="w-full">
            <p v-on:click="click" v-bind:class="{'mb-6': isClicked}" class="md:text-xl font-semibold flex justify-between cursor-pointer transition-all duration-300">
                <span class="my-auto">{{title}}</span>
                <span  class="my-auto">
                    <svg
                        v-bind:class="{'rotate-180': isClicked, 'rotate-0': !isClicked }"
                        xmlns="http://www.w3.org/2000/svg" 
                        viewBox="0 0 12 6" 
                        class="transform transition duration-300 w-6 text-gray-a6 stroke-current items-center"
                    >
                        <path fill="none" stroke-linecap="round" d="M1 .5l5 5 5-5" stroke="currentColor"></path>
                    </svg>
                    
                </span>
            </p>

            <div v-bind:style="{height: !isClicked ? '0' : '46px'}" class="md:border-l-8 md:pl-6 border-grey text-sm transition-all duration-300 overflow-hidden">
                <p class="font-medium mb-1">{{ subTitle}}</p>
                <p>{{content}}</p>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name:'FaqItem',
    props:["title","subTitle" ,"content", "index"],
    data(){
        return {isClicked: this.$props.index===0}
    },

    methods:{
        click: function(){
            this.isClicked=!this.isClicked
        }
    }
};
</script>

<style>
    .grey{
        background-color: #e9eaf2;
    }
    .lightgrey{
        background-color: #f6f6f6;
    }
    .border-grey{
        border-left: 8px solid #e0e1ec;
    }

</style>