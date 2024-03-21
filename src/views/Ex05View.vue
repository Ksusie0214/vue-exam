<template>
    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>

    <form v-on:submit.prevent="getPersonVo" action="/mysite/updateperson" method="get">
        <label for="uName">이름</label>
        <input id="uName" type="text" name="name" v-model="personVo.name">
        <br>
        <label for="uHp">전화번호</label>
        <input id="uHp" type="text" name="hp" v-model="personVo.hp">
        <br>
        <textarea name="content" id="" v-model="personVo.content"></textarea>
        <br>
        <button v-on:click="setPersonVo" type="button">값쓰기</button>
        <button button="submit">값 수정</button>
    </form>
</template>

<script>
export default {
    name: "Ex05View",
    components: {},
    data() {
        return {
            title: "Vue공부",
            subTitle: "폼-txt, textarea : (양방향바인딩)-> 폼에는 v-model 그냥 쓰자",
            personVo: {
            name:"",
            hp:"",
            content:""
            }
        };
    },
    methods: {
        setPersonVo(){
            let pVo={
                name: "정우성",
                hp: "010-2222-2222",
                content: "영화배우 정우성입니다."
            }
            this.personVo= pVo;
            /*
            console.log("클릭");
            this.name="정우성",
            this.hp="010-2222-2222",
            this.content="영화배우 정우성입니다."
            */
        },
        getPersonVo(){
            console.log("데이터 수집");
            console.log("서버로 전송.......");

            console.log(this.personVo);
        }
    },
};
</script>
<style></style>