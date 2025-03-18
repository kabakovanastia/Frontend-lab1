<template>
    <head>
        <meta charset="UTF-8" />
        <title>lab1</title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap" rel="stylesheet">
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
                <h1 class="title">Заголовок основного блока</h1>
                <img class="main-pic" id="pic" src='require("./static/pic1")'/>
                <button @click="changePic">Поменять картинку</button>
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
<!-- <script setup>
    import {ref} from 'vue';
    const pic1 = ref("./assets/pic1.jpg")
    function changePic() {
        if (pic1.value == "./assets/pic1.jpg"){
            pic1.value = "./assets/pic2.jpg";
        } else {
            pic1.value = "./assets/pic1.jpg";
        }
    }
</script> -->
<style scoped>
.main-cont {
    display: flex;
    flex-direction: column;
    height: 97vh;
    font-size: 1.6rem;
    font-family: Open Sans, sans-serif;
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
    font-family: Montserrat, sans-serif;
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
.title {
    flex-grow: 1;
}
.main-pic {
    height: 200px;
}

button {
    width: 55%;
    font-size: 1.6rem;
    font-family: Open Sans, sans-serif;
}
</style>