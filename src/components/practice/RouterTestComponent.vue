<template>
    <div>
        <h1>화면 라우팅 테스트</h1>
        <div>
            <v-btn @click="spaMove1">modeling 페이지로 이동(url)</v-btn>
        </div>
        <div>
            <v-btn @click="spaMove2">modeling 페이지로 이동(name)</v-btn>
        </div>
        <div>
            <v-btn @click="hrefMove">modeling 페이지로 이동(href)</v-btn>
        </div>
        <div>
            <v-btn @click="reloadPage">현재화면 reload</v-btn>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        spaMove1() {
            this.$router.push("/practice/modeling");
        },
        spaMove2() {
            this.$router.push({ name: "ModelingComponent" });
        },
        hrefMove() {
            window.location.href = '/practice/modeling';
        },
        // 화면 새로고침과 같은 기능
        reloadPage() {
            window.location.reload();
        }
    }
}
</script>