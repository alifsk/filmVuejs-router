<template>
    <div class="container">
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" v-if="filmId == data.id">
                <h1 class="page-title">Movie Details</h1>
                <img v-bind:src="data.image"  class="img-fluid img-movie" v-bind:alt="data">
                <div class="value">
                    <h1>{{data.title}}</h1>
                    <hr>
                    <p class="desc">{{data.desc}}</p>
                    <h2>IMDb : {{data.rating}}</h2>
                    <p>Genre : {{data.genre}}</p>
                    <p>Duration : {{data.duration}}</p>
                    <p>Director : {{data.director}}</p>
                    <p>Actor : {{data.actor}}</p>
                    <p>Release : {{data.release}}</p>
                    <p>Country : {{data.country}}</p>
                </div>
            </div>
        </div>
        <div class="back">
            <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
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
  data() {
    return {
      filmId: this.$route.params.id,
      movie: [
        {
          id: 1,
          image: Img1,
          desc: ' Bagi Nathan (Jefri Nichol) dan Salma (Amanda Rawles) tidak ada yang lebih indah selain cinta mereka, tetapi Ayah Salma melarang hubungan mereka dan Salma dijodohkan dengan Ridho (Devano Danendra). Apalagi ketika Nathan berkelahi yang membuat mereka salah paham dan Nathan pindah sekolah hingga akhirnya Salma memutuskan hubungan Nathan. Nathan bertemu dengan Rebeca (Susan Sameh) yang jatuh cinta dengan Nathan. Salma yang tertekan oleh Ayahnya gara-gara gagal amasuk UI bertemu Rebeca yang membantunya keluar dari keputusasaannya. Tetapi pertemuannya dengan Rebeca justru membuatnya bertemu kembali dengan Nathan.',
          title: 'Dear Nathan: Hello Salma (2018)',
          rating: '8.4',
          genre: 'Drama, Romance',
          release: '2018',
          duration: '101 min',
          director: 'Indra Gunawan',
          actor: ' Amanda Rawles, Devano Danendra, Diandra Agatha, Jefri Nichol, Karina Suwandi, Surya Saputra, Susan Sameh',
          country : 'Indonesia'
        },
        {
          id: 2,
          image: Img2,
          desc: 'Risa tinggal bersama adiknya Riri yang sudah mulai bosan dengan kemampuan Risa yang mampu melihat hantu. Mereka berdua sering menginap ditempat pamannya Om Ahmad (Bucek Depp) dan tantenya Tina (Sophia Latjuba). Tetapi mereka berdua merasa ada yang janggal dirumah tersebut, apalagi Om Ahmad bersikap aneh.',
          title: 'Danur 2: Maddah (2018)',
          rating: '6.7',
          genre: ' Horror, Thriller',
          release: '2018',
          duration: '92 min',
          director: ' Awi Suryadi',
          actor: 'Bucek, Elena V. Holovcsak, Prilly Latuconsina, Sandrinna Michelle, Shareefa Daanish, Shawn Adrian Khulafa, Sophia Latjuba',
          country : 'Indonesia'
        },
        {
          id: 3,
          image: Img3,
          title: 'Mata Batin (2017)',
          desc: 'Setelah saudara perempuannya meninggal, Alia memutuskan untuk memulai hidup baru dengan tinggal di panti asuhan milik Ny. Laksmi dan Tuan Fadli serta melakukan pekerjaan sosial di sana. Tapi Alia merasa ada yang salah dengan panti asuhan. Selain itu, Nadia, salah satu panti asuhan yang tampaknya juga memiliki mata batin seperti Alia, dapat mendengar suara-suara misterius yang meminta bantuan dari seluruh dinding rumah. Alia dan Nadia membuka ruang terkunci yang misterius. Sejak itu bencana dimulai. Ternyata Alia dan Nadia telah melakukan kesalahan besar dan melepaskan Darmah, roh pendendam yang sengaja dikunci di dalam ruangan. Bersama Ny. Windu, paranormal dan mentor mata batinnya, Alia harus berhadapan dengan Darmah dan menyelamatkan panti asuhan.',
          rating: '6.5',
          genre: 'Horror, Mystery, Thriller',
          release: '2017',
          duration: '116 min',
          director: 'Rocky Soraya',
          actor: ' Bianca Hello, Citra Prima, Jelita Callebaut, Jeremy Thomas, Jessica Mila, Nabilah Ratna Ayu, Sophia Latjuba.',
          country : 'Indonesia'
        },
        {
          id: 4,
          image: Img4,
          title: 'Filosofi Kopi (2019)',
          desc: 'Cerita tentang pencarian jiwa dan perjalanan berdamai dengan masa lalu melalui kopi. Ben dan Jody adalah sahabat yang membangun kedai “Filosofi Kopi”, sebuah kedai kopi terkemuka di Jakarta yang hanya menyediakan kopi terbaik Indonesia. Sebuah tantangan untuk membuat kopi yang sempurna dari seorang pengusaha membawa Ben dan Jody pada petualangan menyusun serpihan masa lalu mereka yang penuh getir dengan orang tua mereka masing-masing.',
          rating: '7.1',
          release: '2019',
          duration: '117 min',
          genre: 'Adventure, Comedy, Drama',
          director: 'Angga Dwimas Sasongko',
          actor: ' Chicco Jerikho, Jajang C. Noer, Julie Estelle, Otig Pakis, Rio Dewanto, Ronny P. Tjandra, Slamet Rahardjo.',
          country : 'Indonesia'
        },
        {
          id: 5,
          image: Img5,
          title: 'Surat Cinta Untuk Starla The Movie (2017)',
          desc: 'Hema sangat mencintai alam. Dia menulis surat cinta ke alam menggunakan mesin tiknya. Dia juga membuat mural untuk menunjukkan cintanya pada alam. Suatu hari, dia bertemu Starla. Dalam 6 jam, dia jatuh cinta pada gadis ini. Hema menyadari bahwa ada lebih dari sekadar alam untuk dicintai. Hema dan Starla semakin dekat. Sampai Starla mulai menjauh dari Hema.',
          rating: '6.2',
          release: '2017',
          duration: '90 min',
          genre: 'Drama, Romance',
          director: 'Rudi Aryanto',
          actor: 'Caitlin Halderman, Erwin Bagindo, Jefri Nichol, Salshabilla Adriani.',
          country : 'Indonesia'
        },
        {
          id: 6,
          image: Img6,
          title: 'Rasuk 2 (2020)',
          desc: 'Isabella (Nikita Willy), mahasiswi kedokteran yang sedang menjalani koas, merasa tidak nyaman dengan kemampuan indera keenam yang dimilikinya. Dia berupaya kuat menganggap mereka tidak ada agar bisa hidup dengan normal. Namun, kejadian di ruang autopsi saat membedah satu jenazah wanita tanpa identitas mengubah semua pandangan hidupnya. Arwah jenazah itu terus mengikutinya, meneror, bahkan merasukinya untuk meminta tolong. Kondisi ini mengganggu hubungan Isabela dengan teman-temannya dan mengancam studinya. Satu-satunya orang yang bisa memahami Isabela dan memberinya dukungan adalah sang kakak, Fransisca Inggrid (Raquel Katie Larkin). Di tengah usahanya melepaskan diri dari gangguan gaib yang mengancam jiwanya, Isabela jatuh cinta dengan Radja (Achmad Megantara). Untuk pertama kali dalam hidupnya, Isabela bertemu dengan seseorang yang bisa memahami kelebihannya selain Fransisca Inggrid. Gangguan yang dialami Isabela membawanya menguak selembar demi selembar misteri tentang kematian sang arwah yang mengganggunya selama ini. Tidak ada pilihan bagi Isabela selain menerima kelebihannya, dan membantu sang arwah menyelesaikan urusannya. Meskipun ia harus mempertaruhkan keselamatan jiwanya..',
          rating: '7.0',
          release: '2020',
          duration: '100 min',
          genre: 'Horor, Mystery, Thriller',
          director: 'Rizal Mantovani',
          actor: 'Nikita Willy, Achmad Megantara, Asri Welas, Raquel Katie Larkin, Sonia Alyssa, Prilly Latuconsina, Tegar Satrya, Iang Darmawan.',
          country: 'Indonesia'
        },
        {
          id: 7,
          image: Img7,
          title: 'Sri Asih (2020)',
          desc: 'Nani Wijaya adalah seorang gadis lugu yang terlahir dari keluarga kaya raya. Ia merupakan reinkarnasi dari Dewi Sri. Apabila ia mengucapkan kata sakti "Dewi Asih", maka ia akan berubah menjadi Sri Asih, seorang pahlawan super wanita yang memiliki keahlian bela diri yang memiliki kekuatan setara dengan 250 pria dewasa.[1] Tak hanya itu, Sri Asih juga memiliki kemampuan untuk terbang, memiliki tubuh yang kebal, serta memiliki Triwikarma, sebuah kemampuan titisan Dewa Wisnu yang membuatnya dapat menggandakan diri dan dapat memperbesar tubuhnya.',
          rating: 'Coming Soon',
          release: 'Coming Soon 2020',
          duration: '-',
          genre: 'Action, Crime, Drama',
          director: 'Upi Avianto',
          actor: 'Pevita Pearce, Chelsea Islan, Chicco Jerikho, Joe Taslim, Nicholas Saputra .',
          country: 'Indonesia'
        },
        {
          id: 8,
          image: Img8,
          title: 'Gundala (2019)',
          desc: 'Sancaka telah hidup di jalanan sejak orang tuanya meninggalkannya. Menjalani hidup yang sulit, Sancaka bertahan dengan memikirkan keselamatannya sendiri. Ketika kondisi kota semakin memburuk dan ketidakadilan mengamuk di seluruh negeri, Sancaka harus memutuskan apakah ia terus hidup untuk menjaga dirinya sendiri atau bangkit untuk menjadi pahlawan bagi yang tertindas.',
          rating: '7.8',
          release: '2019',
          duration: '123 min',
          genre: 'Joko Anwar',
          director: 'Joachim Rønning, Espen Sandberg',
          actor: 'Abimana Aryasatya, Bront Palarae, Fariz Fajar, Marissa Anita, Muzakki Ramdhan, Rio Dewanto, Tara Basro.',
          country: 'Indonesia'
        },
      ],
    };
  },
};
</script>

<style scoped>
    .container {
        width: auto;
    }
    .header-title {
      font-family: monospace;
      font-size: 70px;
      color: #deda9e;
    }
    .header-subtitle {
      font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
      font-size: 20px;
    }
    .movie-item {
        padding: 50px;
        width: auto;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: minmax(50px, auto);
        text-align: left;
        background-color: #560D13;
    }
    .page-title {
        grid-column: 1/3;
        text-align: center;
        padding-bottom: 30px;
        background-color: #560D13;
        font-family: 'Times New Roman', Times, serif;
        border: 0px;
        border-radius: 20px;
    }
    .back {
      text-align: center;
      padding-bottom: 50px;
      background-color: #560D13;
    }
    .btn-back {
        background-color: red;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn-back:hover {
        background-color: transparent;
        border: 2px solid red;
        color: red;
    }
    .img-movie {
        width: 500px;
        box-shadow: 0 20px 25px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
        border: 0px;
        border-radius: 20px;
    }
    .desc {
        text-align: justify;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #000;
        color: #fff;
        text-align: center;
    }
    .value{
      color: #fff;
      font-family: 'Times New Roman', Times, serif;
    }
    h1{
      font-size: 50px;
      padding-top: 50px;
    }
    .page-title{
      color:#fff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
      transition: 0.3s;
      background-color: #181818;
      width: 100%;
      height: 100px;
    }
</style>