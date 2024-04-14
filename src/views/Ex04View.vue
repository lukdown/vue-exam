<template>
    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>

    <div class="box" v-bind:class="{ 'box-red': isRed, 'box-blue': isBlue, 'f-bold': isBold, 'f-big': isSize, 'f-ita': isStyle }">
        {{ boxText }}
    </div>

    <button v-on:click="redBox" type="button">빨간박스</button>
    <button v-on:click="blueBox" type="button">파란박스</button>
    <button v-on:click="boldOnOff" type="button">볼드on/off</button>
    <button v-on:click="sizeOnOff" type="button">크기on/off</button>
    <button v-on:click="styleOnOff" type="button">스타일on/off</button>

    <br><br><br><br>
    <p style="color: red;">인라인스타일로 태그에 스타일 직접 추가</p>
    
    <p v-bind:style="type">인라인스타일로 태그에 스타일 직접 추가</p>
    <button v-on:click="changeType" type="button">인라인 스타일 변경</button>

</template>

<script>
export default {
    name: "Ex04View",
    components:{},
    data() {
        return {
            title: "Vue공부",
            subTitle: "class속성 제어",
            boxText: "vue공부 재미없어요",
            isRed: false,
            isBlue: false,
            isBold: false,
            isSize: false,
            isStyle: false,
            type: ""
        };
    },
    methods: {
        redBox(){
            this.isRed = true;
            this.isBlue = false;
        },
        blueBox(){
            this.isRed = false;
            this.isBlue = true;
        },
        boldOnOff() {
            console.log("볼드 클릭");
            if(this.isBold == true){
                this.isBold = false;
            }else{
                this.isBold = true;
            }
        },
        sizeOnOff(){
            this.isSize = !this.isSize;
        },
        styleOnOff(){
            this.isStyle = !this.isStyle;
        },
        changeType() {
            console.log("클릭");
            this.type= "font-size: 20px; color: red;";
        }

    },
};
</script>

<style>
.box{
    width: 150px;
    border: 1px solid black;
}

.box-red{
    background-color: red;
}

.box-blue{
    background-color: blue;
}

.f-bold{ font-weight: bold; }

.f-big{ font-size: 20px; }

.f-ita{ font-style: italic; }

</style>