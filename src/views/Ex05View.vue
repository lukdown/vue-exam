<template>
    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>

    <!-- form 전송 클릭이벤트와 다르다 form 에 submit 이벤트 -->
    <form v-on:submit.prevent="getPersonVo" action="" method="get">
        <label for="uName">이름: </label>
        <input id="uName" type="text" name="name" v-model="personVo.name">
        <br>
        <label for="uHp">전화번호: </label>
        <input id="uHp" type="text" name="hp" v-model="personVo.hp">
        <br>
        <textarea name="content" id="uContent" v-model="personVo.content" cols="30" rows="10"></textarea>

        <br><br>
        <button v-on:click="setPersonVo" type="button">값쓰기</button>
        <button type="submit">값 수정</button>
    </form>

    <p></p>
</template>

<script>

export default {
    name: "Ex05View",
    components:{},
    data() {
        return {
            title: "Vue공부",
            subTitle: "폼-text, textarea: (양방향바인딩)->폼에는 v-model 그냥쓰자",
            personVo: {
                name: "",
                hp: "",
                content: ""
            }

        };
    },
    methods: {
        setPersonVo() {
            console.log("서버로부터 데이터를 받는중 .............");
            
            let pVo= {
                name : "정우성",
                hp : "010-1234-5678",
                content : "배고파"
            };
            this.personVo = pVo;

        },
        getPersonVo(){

            console.log("데이터수집...........");
            console.log(this.personVo);

        }
    },
};
</script>

<style>

</style>

