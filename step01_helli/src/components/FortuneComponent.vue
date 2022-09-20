<!-- FortuneComponent.vue -->
<template>
    <div>
        <p>오늘의 운세 : <strong>{{fortune}}</strong></p>
    </div>
</template>

<script>
export default{
    namd:"FortuneComponent",
    props:{
        //fortune 이라는 이름의 property 를 받을예정이고 type 은 String 으로 고정
        fortune:String
    }
}
</script>

<style>
    strong{
        color:red
    }
</style>