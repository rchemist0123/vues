<template>
    <div>
        <h1>Users Detail</h1>
        <p>유저번호: {{ userId }}</p>
        <v-btn @click="edit">수정</v-btn>
    </div>
</template>
<script>
export default {
    computed:{
        userId(){
            return this.$route.params.id
        }
    },
    methods: {
        edit(){
            // this.$router.push({name: 'users-edit'})
             this.$router.push({path: `${this.userId}/edit`})
            //  경로가 users에서 시작되기 떄문에 path 시작점에 users를 붙이면 안됨.
        }
    }
}
</script>