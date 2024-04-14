<template>

    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>

    <select name="telecom" id="">
        <option value="">이동통신사를 선택해주세요</option>
        <option value="sk" selected="selected">SK텔레콤</option>
        <option value="kt">KT</option>
        <option value="lg">LG U+</option>
    </select>

    <br><br>
    <select name="telecom" id="" v-model="telecom">
        <option value="">이동통신사를 선택해주세요</option>
        <option value="sk">SK텔레콤</option>
        <option value="kt">KT</option>
        <option value="lg">LG U+</option>
    </select>
    <p>선택한 이동통신사는 {{ telecom }}입니다</p>

    <p></p>
</template>
<script>

export default {
    name: "Ex06View",
    components: {},
    data() {
        return {
            title: "vue 공부시작",
            subTitle: "폼-selectbox: (양방향바인딩)->폼에는 v-model 그냥쓰자",
            telecom: "lg"
        };
    },
    methods: {}
};
</script>
<style></style>