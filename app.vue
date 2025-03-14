<template>
    <head>
       <meta charset="UTF-8" />
       <title>lab1</title>
    </head>

    <div class="main-cont">
        <div class="header">
            <span>Текст для хедера</span>
        </div>
        <div class="main">
            <div class="list">
                <span>Заголовок списка</span>
                <ul>
                    <li>Опция 1</li>
                    <li>Опция 2</li>
                    <li>Опция 3</li>
                </ul>
            </div>
            <div class="main-block">
                <h1 class="header-text">Заголовок основного блока</h1>
                <span class="header-span" id="text">{{string1}}</span>
                <button @click="changeText">Поменять приветствие</button>
            </div>
            <div class="third-block">
                <span>Наполнение третьего блока</span>
            </div>
        </div>
        <div class="footer">
            <span>Ссылки для связи, информация об авторе</span>
        </div>
    </div>
</template>
<script setup>
    import {ref} from 'vue';
    const string1 = ref('Hello, world!')
    function changeText() {
        if (string1.value == "Hello, world!"){
            string1.value = "Hello, FEFU!";
        } else {
            string1.value = "Hello, world!";
        }
    }
</script>
<style scoped>
.main-cont {
    display: flex;
    flex-direction: column;
    height: 97vh;
    font-size: 1.6rem;
}
.header {
    background-color: #93D7E4;
    margin: 10px;
    height: 15%;
    padding: 10px;
    align-content: center;
}
.main {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-grow: 1;
}
.list {
    width: 20%;
    background-color: #57AF7B;
    margin: 10px;
    padding: 10px;
}
.main-block {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    background-color: #F4BF55;
    margin: 10px;
    padding: 10px;
    align-items: center;
}
.third-block {
    width: 20%;
    background-color: #57AF7B;
    margin: 10px;
    padding: 10px;
}
.footer {
    background-color: #1598AC;
    margin: 10px;
    height: 15%;
    padding: 10px;
    align-content: center;
}
.header-text {
    flex-grow: 1;
}
.header-span {
    text-align: center;
    margin: 20px;
}
button {
    width: 55%;
    font-size: 1.6rem;
}
</style>