<template>
    <div class="container">
        <div class="header">
            <div class="card">
                <h1 class="header-title">VUEFLIX</h1>
                <h3 class="header-subtitle">Watch Vueflix movies & TV shows online or stream right to your smart TV, game console, PC, Mac, mobile, tablet and more.</h3>
                <h3 class="header-subtitle">Relax, Stay Calm, and Enjoy for Watching.</h3>
            </div>
        </div>
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" @click="detailfilm(data.id)">
                <img v-bind:src="data.image" class="img-fluid img-movie" v-bind:alt="data">
            </div>
            <h1>{{data.title}}</h1>
            <div class="detail">
                <button class="btn-detail" @click="detailfilm(data.id)">Detail</button>
            </div>
        </div>
        <div class="footer">
            <h5>Build &copy;2020. By Kurniawan film</h5>
        </div>
    </div>
</template>

<script>
import Img1 from '../assets/images/1.jpg';
import Img2 from '../assets/images/2.jpg';
import Img3 from '../assets/images/3.jpg';
import Img4 from '../assets/images/4.jpg';
import Img5 from '../assets/images/5.jpg';
import Img6 from '../assets/images/6.jpg';
import Img7 from '../assets/images/7.jpg';
import Img8 from '../assets/images/8.jpeg';

export default {
  data: () => ({
    movie: [
      { id: 1, title: 'Dear Nathan: Hello Salma (2018)', image: Img1 },
      { id: 2, title: 'Danur 2: Maddah (2018)', image: Img2 },
      { id: 3, title: 'Mata Batin: Believing Is Seeing (2017)', image: Img3 },
      { id: 4, title: 'Filosofi Kopi (2019)', image: Img4 },
      { id: 5, title: 'Surat Cinta untuk Starla (2017)',  image: Img5 },
      { id: 6, title: 'Rasuk 2 (2020)', image: Img6 },
      { id: 7, title: 'Sri Asih (2020)', image: Img7 },
      { id: 8, title: 'Gundala (2019)', image: Img8 }
    ],
  }),
  methods: {
    detailfilm(filmId) {
      this.$router.push({ name: 'detail', params: { id: filmId } });
    },
  },
};
</script>

<style scoped>
    .container {
        width: auto;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: minmax(50px, auto);
        background-color: #560D13;
    }
    .header {
        padding: 50px;
        grid-column: 1/5;
        background-color: #560D13;
        color: #fff;
        text-align: left;
    }
    .header-title {
      font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
      font-size: 70px;
      text-align: center;
      padding-top: 50px;
      color: red;
    }
    .header-subtitle {
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        font-size: 20px;
        color: #fff;
        text-align: center;
    }
    .card {
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
        background-color: #181818;
        width: 100%;
        height: 300px;
        border: 0px;
        border-radius: 20px;
    }
    .card:hover {
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #000;
        color: #fff;
        text-align: center;
    }
    .movie {
        padding-top: 60px;
        padding-bottom: 60px;
        text-align: center;
        background-color: #560D13;
    }
    .img-movie {
        width: 250px;
        box-shadow: 0 20px 35px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
        border: 0px;
        border-radius: 20px;
    }
    .img-movie:hover{
        box-shadow: 0 40px 45px 0 rgba(0,0,0,0.2);
    }
    .detail {
      text-align: center;
      padding-bottom: 50px;
      background-color: #560D13;
    }
    .btn-detail {
        background-color: transparent;
        color: red;
        font-size: 30px;
        text-align: center;
        cursor: pointer;
        border: 0;
        width: 80px;
    }
    h1{
        color: #fff;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }
</style>