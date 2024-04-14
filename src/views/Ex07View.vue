<template>

    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>


    <label for="">10대</label><input type="radio" name="age" value="10" v-model="picked">
    <label for="">20대</label><input type="radio" name="age" value="20" v-model="picked">
    <label for="">30대</label><input type="radio" name="age" value="30" v-model="picked">
    <label for="">기타</label><input type="radio" name="age" value="etc" v-model="picked">
    <p>당신의 나이는 {{ picked }}입니다</p>
    
    <br><br><br>
    <label for="">독서</label><input type="checkbox" name="hobby" value="book" v-model="checked">
    <label for="">여행</label><input type="checkbox" name="hobby" value="trip" v-model="checked">
    <label for="">게임</label><input type="checkbox" name="hobby" value="game" v-model="checked">
    <label for="">잠자기</label><input type="checkbox" name="hobby" value="sleep" v-model="checked">
    <p>선택한 취미는 {{ checked }}입니다</p>
    
</template>
<script>

export default {
    name: "Ex07View",
    components: {},
    data() {
        return {
            title: "vue 공부시작",
            subTitle: "폼-radio, checkbox: (양방향바인딩)->폼에는 v-model 그냥쓰자",
            picked: "30",
            checked: ["book", "game"]
        };
    },
    methods: {}
};
</script>
<style></style>