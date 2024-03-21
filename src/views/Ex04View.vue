<template>
    <h1>{{title}}</h1>
    <h2>{{subTitle}}</h2>
    <div class="box" v-bind:class="{'box-red':isRed, 'box-blue':isBlue, 'f-bold':isBold, 'f-size':isSize, 'f-italic':isItalic}">{{ boxText }}</div>
    <button v-on:click="redBox" type="button">빨간박스</button>
    <button v-on:click="blueBox" type="button">파란박스</button>
    <button v-on:click="boldOnOff" type="button">볼드 on/off</button>
    <button v-on:click="sizeOnOff" type="button">크기 on/off</button>
    <button v-on:click="italicOnOff" type="button">이탤릭체 on/off</button>

    <br><br><br><br>
    <p style="font-size:30px">인라인스타일로 태그에 스타일 직접 추가</p>
    <p>인라인스타일로 태그에 스타일 직접 추가</p>
    <button v-on:click="changeType" type="button">인라인 스타일 변경</button>
</template>

<script>
export default {
    name: "Ex04View",
    components: {},
    data() {
        return {
            title : "Vue 공부",
            subTitle: "class속성 제어",
            boxText : "Vue공부 재미있습니다",
            isRed: false,
            isBlue: false,
            isBold: false,
            isSize: false,
            isItalic: false,
            type:""
        };
    },
    methods: {
        redBox(){
            this.isRed=true;
            this.isBlue=false;
        },
        blueBox(){
            this.isBlue=true;
            this.isRed=false;
        },
        boldOnOff(){
            console.log("온오프");
            if(this.isBold==true){
                this.isBold=false;
            }else{
                this.isBold=true;
            }
        },
        sizeOnOff(){
            if(this.isSize==true){
                this.isSize=false;
            }else{
                this.isSize=true;
            }
        },
        italicOnOff(){
            if(this.isItalic==true){
                this.isItalic=false;
            }else{
                this.isItalic=true;
            }
        },
        changeType(){
            console.log("클릭");
            this.type="color:#ff0000";
        }
    },
};
</script>
<style>
    .box{
        width: 150px;
        border : 1px solid #000000;
    }
    .box-red{
        background-color: #ff0000;
    }
    .box-blue{
        background-color: #0000ff;
    }
    .f-bold{
        font-weight: bold;
    }
    .f-size{
        font-size: 20px;
    }
    .f-italic{
        font-style: italic;
    }

</style>