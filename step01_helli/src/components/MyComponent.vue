<template>
    <div class="bg-yellow">
        <p>나의 컴포넌트 입니다.</p>
        <p>author : <strong>{{author}}</strong></p>
    </div>
</template>
<script>
//각각의 컴포넌트는 고유한 모델과 동작을 가질수 있다.
export default{
    //디버깅의 편의를 위해 이름을 지정하는데 보통 파일의 이름과 같게 짓는다.
    name:'MyComponent',
    data(){
        return {
            author:'김구라'
        };
    }
}
</script>
<!-- scoped 속성을 가진 style 은 해당 component 에서만 적용되는 css 이다. -->
<style scoped>
    .bg-yellow{
        background-color: yellow;
    }
</style>