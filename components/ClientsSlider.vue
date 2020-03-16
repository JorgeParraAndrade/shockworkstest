<template>
  <div class="container">
    <section class="client-slider">
      <h3><span>What Our</span> Client Says?</h3>
      <div class="client-slider-container">
        <div id="pic1" class="profile-pic">
          <img :src="`https://picsum.photos/200/200?random=${users[0].id}`" alt="team">
        </div>
        <div id="pic2" class="profile-pic">
          <img :src="`https://picsum.photos/200/200?random=${users[1].id}`" alt="team">
        </div>
        <div id="pic3" class="main-slide">
          <img :src="`https://picsum.photos/200/200?random=${users[2].id}`" alt="team">
          <p class="slide-quote">
            {{ users[2].company.catchPhrase }}
          </p>
          <div class="meta">
            <h4>{{ users[2].name }}</h4>
            <p>{{ users[2].company.bs }}</p>
          </div>
          <div class="pos-slider-control">
            <button class="btn-slider" @click="moveforward()" ><img src="../assets/img/larrow.png" alt="prev"></button>
            <button class="btn-slider" @click="moveback()" ><img src="../assets/img/rarrow.png" alt="next"></button>
          </div>
        </div>
        <div id="pic4" class="profile-pic">
          <img :src="`https://picsum.photos/200/200?random=${users[3].id}`" alt="team">
        </div>
        <div id="pic5" class="profile-pic">
          <img :src="`https://picsum.photos/200/200?random=${users[4].id}`" alt="team">
        </div>
      </div>
    </section>

  </div>
</template>

<script>
import Image1 from '../assets/img/team1.png' 
import Image2 from '../assets/img/team2.png' 
import Image3 from '../assets/img/team3.png' 
import Image4 from '../assets/img/team4.png' 
import Image5 from '../assets/img/team5.png' 
export default {
  data() {
    return{
      clients: [
        {name:'Jorge Parra', title: 'Ingeniero', desc:'Shokworks are dedicated and they accomplished all my ideas and thoughts for my project, excellent guidance.', image: Image1},
        {name:'Julio Monalgas', title: 'Diseñador', desc:'Shokworks are dedicated and they accomplished all my ideas and thoughts for my project, excellent guidance.', image: Image2},
        {name:'Eduardo Gonzalez', title: 'Ingeniero', desc:'Shokworks are dedicated and they accomplished all my ideas and thoughts for my project, excellent guidance.', image: Image3},
        {name:'Maria Estefania Carruyo', title: 'Redactor', desc:'Shokworks are dedicated and they accomplished all my ideas and thoughts for my project, excellent guidance.', image: Image4},
        {name:'Ignacio Redondo', title: 'Marico', desc:'Shokworks are dedicated and they accomplished all my ideas and thoughts for my project, excellent guidance.', image: Image5}
      ]
    }
  },

  props:['users'],

  methods: {
    moveback(){
      const elem1 = this.users.shift();
      this.users.push(elem1);
    },
    moveforward(){
      const elem1 = this.users.pop();
      this.users.unshift(elem1);
    }
  },

}
</script>

<style lang="scss">
.client-slider {
  h3 {
    text-align: center;
    font-size: 43px;
    margin-top: 70px;
    font-family: montserrat;
    margin-top: 130px;

    span {
      font-weight: 400;
    }
  }

  .client-slider-container {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    margin: 30px 0 130px;

    .profile-pic {
      transition: all ease 0.3s;
      img {
        border-radius: 100px;
      }
    }

    .main-slide {
      width: 100%;
      max-width: 500px;
      text-align: center;

      img {
        width: auto;
        height: 180px;
        border-radius: 100px;
      }

      .meta {
        h4 {
          font-weight: 500;
        }

        p {
          margin: 15px 0 20px;
          font-size: 14px;
          font-weight: 400;
        }
      }

      .slide-quote {
        position: relative;
        &:before {
          content: "";
          position: absolute;
          width: 40px;
          height: 40px;
          background-image: url('../assets/img/quote1.png');
          background-position: center;
          background-size: contain;
          background-repeat: no-repeat;
          top: -25px;
          left: -50px;
        }

        &:after {
          content: "";
          position: absolute;
          width: 40px;
          height: 40px;
          background-image: url('../assets/img/quote2.png');
          background-position: center;
          background-size: contain;
          background-repeat: no-repeat;
          top: -25px;
          right: -50px;

        }

        @media (max-width: 768px) {
          &:before, &:after {
            display: none;
          }
        } 
      }

      .pos-slider-control {
        .btn-slider {
          background-color: none;
          box-shadow: none;

          img {
            width: 18px;
            height: 18px;
          }
        }
      }

    }

  }

  #pic1 {
    img {
      width: 75px;
      height: auto;
      margin-bottom: 50px;
    }

    @media (max-width: 768px) {
      display: none;
    }
  }
  #pic2 {
    align-self: flex-end;

    img {
      width: 112px;
      height: auto;
      margin-bottom: 60px;
    }

    @media (max-width: 768px) {
      display: none;
    }
  }
  #pic4 {
    align-self: flex-start;

    img {
      width: 112px;
      height: auto;
      margin-top: 60px;
    }

    @media (max-width: 768px) {
      display: none;
    }
  }
  #pic5 {
    img {
      width: 75px;
      height: auto;
      margin-top: 50px;
    }

    @media (max-width: 768px) {
      display: none;
    }
  }
}
</style>