<template>
  <div class="presentation">
    <div class="container">
      <div class="left">
        <h1 class="title">Qui Suis-je ?</h1>
        <div class="small_description">
          Geek et passionné de musique, j'aime faire des rencontres et partager
          ma joie de vivre avec tous les gens que je rencontre. D'un naturel
          joyeux, je trouve mon dynamisme dans mes projets et dans la volonté
          d'en apprendre toujours plus !
        </div>
        <div class="idea">
          <ul>
            <li>Musicien dans l'âme depuis toujours.</li>
            <li>Développeur/UX Designer passionné.</li>
            <li>Amoureux des rencontres et du savoir.</li>
            <li><a href="cv.pdf" target="_blank">Découvrir mon CV</a></li>
          </ul>
        </div>
      </div>
      <div class="right"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.presentation {
  margin-bottom: 50px;
  .container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    .left {
      .small_description {
        line-height: 28px;
        margin-bottom: 50px;
      }
      width: 55%;
      .idea {
        ul {
          display: flex;
          flex-direction: column;
          li {
            display: flex;
            align-items: center;
            border-top: 1px solid #f6f6f6;
            padding: 15px 0;
            letter-spacing: 1px;
            a {
              color: #000;
              transition: 0.3s;
              &:hover {
                color: #e8371a;
              }
            }
            &:last-child {
              margin-bottom: 0;
              border-bottom: 1px solid #f6f6f6;
            }
            &:before {
              content: "\f105";
              font-family: FontAwesome;
              font-size: 20px;
              font-weight: bold;
              text-decoration: inherit;
              margin-right: 10px;
              color: #01224f;
            }
          }
        }
      }
    }
    .right {
      background-image: url(~assets/img/pictureMe.jpg);
      height: 450px;
      width: 40%;
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      outline: 1px solid #000;
      outline-offset: 8px;
    }
  }
}
@media screen and (max-width: 800px) {
  .presentation {
    margin-bottom: 30px;
    .container {
      .left {
        .small_description {
          margin-bottom: 25px;
        }
        .idea {
          margin-bottom: 25px;
        }
      }
      flex-direction: column;
      .title {
        text-align: center;
      }
      .right {
        width: 100%;
        height: 350px;
        display: flex;
        align-items: center;
        justify-content: center;
        background-size: contain;
      }
    }
  }
}
@media screen and (max-width: 800px) {
  .presentation {
    .container {
      .left {
        width: 100%;
      }
    }
  }
}
</style>