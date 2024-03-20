<template>
    <h1>vue공부</h1>
    <h2>{{ subTitle }}</h2>
    <p>{{ content }}</p>
</template>

<script>
export default {
    name: "Ex01View",
    components: {},
    data() {
        return {
            subTitle: "바인딩된 소제목",
            content : "죽을때까지 끄투하자"
        };
    },
    methods: {},
};
</script>
<style></style>