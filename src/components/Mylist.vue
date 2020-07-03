<template>
    <div class="hello">
        <h1>{{message}}</h1>
        <div>
            <input type="text" v-model="text">
            <button v-on:click="doAction">クリック</button>
        </div>          
    </div>
    
</template>

<script>
    export default{
        name:"Mylist",
        props:{
            title:String,
        },
        data:function(){
            return {
                message:"メモを入力してください",
                text:"",
            };
        },
        methods:{
            doAction:function(){
                var input_text = this.text;
                
                this.$emit("result-event",input_text);
            }
        }
    }
</script>
