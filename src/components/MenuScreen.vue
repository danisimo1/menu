<template>
  <header>
    <div class="container">
      <p><strong>Мой ИЖС</strong><img class="header-logo" src="../assets/logo.jpg" alt="logo"><strong class="header-status">статус</strong></p>
    </div>
  </header>

  <div class="info">
    <span class="info-text">Все инженеры и Росреестр за 0 ₽ — оплатите первый этап строительства до 25 августа и Genius активируется автоматически</span>
    <img class="logo1" src="../assets/logo1.jpg" alt="logo1">
  </div>

  <div class="list">
    <ul v-for="listElement in menuList" v-bind:key="listElement.id">
      <li>{{listElement}}<span class="arrow" @click="''">></span></li><hr>
    </ul>
  </div>

  <div class="navigation">
    <img v-for="pic in pictures" :src="pic.src" v-bind:key="pic"><span class="nav" v-for="navElement in navbar" v-bind:key="navElement">{{navElement}}</span>
  </div>

</template>

<script>
export default {
  name: 'MenuScreen',
  data(){
    return{
      menuList : [
      'Как это работает', 'ИЖС Стандарт' , 'Договоры', 'Росреестр', 'Помощь', 'Промокоды', 'Партнерам', 'Избранное'
    ],
      navbar: [
        'Главное', 'Каталог', 'Landscape', 'Стройка', 'Меню'
      ],
      pictures: [
        // здесь пути для добавлению картинок в списке меню через v-for
        {src: ''},
        {src: ''}
      ]
    }
  }
}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Roboto&family=Roboto+Flex:opsz,wght@8..144,500&display=swap');
  
  template{
    max-width: 500px;
    font-family: 'Roboto Flex', sans-serif;
  }
  .container{
    position: relative;
    width: auto;
  }
  
  .info {
    position: relative;
    background: #000;
    height: auto;
    width: auto;
    border-radius: 15px;
    display: flex;
  }

  .info-text {
    color: white;
    padding: 16px 96px 16px 16px;
    font-size: 11px;
    width: 150px
  }

  .arrow {
    float: right;
    color: #a49d9d;
  }

  .nav {
    margin-left: 20px;
    display: inline;
    width: auto;
  }
  
  .logo1 {
    position: absolute;
    margin: 15px 15px 15px 15px;
    right: 15px;
  }

  .header-logo {
    width: 25px;
    height: 25px;
    position: absolute;
    right: 50px;
  }

  .header-status {
    width: 25px;
    height: 25px;
    position: absolute;
    right: 20px;
  }

  .navigation {
    background: #9A989A;
    position: flex;
    bottom: 30px;
    border-radius: 20px;
    width: auto;
    margin-top: 300px;
  }
</style>