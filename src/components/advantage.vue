<template>
  <div class="row advantage-container">
    <div class="col-lg-5 col-md-12 col-xs-12">
      <div class="main-advantage">
        <h2 class="title-advantage">Les avantages du logiciel RH Apidae</h2>
        <br/>
        <span class="main-text">
          Apidae est une solution de gestion d'entreprise facile à mettre en place au sein de vos équipes.
          Apidae vous accompagne dans la digitalisation des tâches administratives pour faciliter la gestion du
          personnel. Avec Apidae vous faites gagner du temps à tous vos collaborateurs &nbsp;!
        </span>
        <br/>
        <div class="place-button">
          <a class="btn btn-lg btn-yellow col-xs-12" v-if="showbtntry" @click="scroll_to_signup">Essayez dés maintenant</a>
        </div>
      </div>
    </div>
    <div class="col-lg-7 col-md-12 col-xs-12 row">
      <product-advantage v-for="product in productAdvantages" :key="product.title"
             class="col-xs-12 col-md-6 col-lg-6">
          <span slot="title">{{product.title}}</span>
          <p class="advantage" slot="advantage">{{product.advantage}}</p>
          <p class="advantage" slot="advantage2">{{product.advantage2}}</p>
      </product-advantage>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  import ProductAdvantage from "./product-advantage";

  export default {
    components: {
      ProductAdvantage
    },
    props: {
      showbtntry: {type: Boolean, required: true},
      scroll_to_signup: {type: Function, required: true}
    },
    data () {
      return {
        productAdvantages: [
          {
            title: "SIMPLE D'UTILISATION",
            advantage:
                "Conscinet que le changement peut être difficile à adopter, les équipes de Apidae " +
                "ont mis en place un logiciel RH facile à prendre en main, son interface ergonomique " +
                "vous permet de l'installer rapidement au sein de votre entreprise. Vos équipes " +
                "pourront prendre en main l'outil rapidement."
          },
          {
            title: "NOTRE ACCOMPAGNEMENT",
            advantage:
                "Un logiciel adaptable à vos besoins : Une équipe travaille constamment sur le " +
                "déveleppement de l'application Apidae pour répondre favorablement à vos " +
                "besoins !",
            advantage2:
                "Vous pouvez contacter le support technique rapidement par mail ou " +
                "par téléphone. Une équipe vous répond le plus rapidement possible."
          },
          {
            title: "GAGNER EN PRODUCTIVITÉ ET EFFICACITÉ :",
            advantage:
                "Gagner en productivité en intégrant notre SIRH dans votre entreprise. Faites gagner " +
                "du temps à chaque menbre de votre équipe, en centratisant les tâches administratives " +
                "sur une seule application RH."
          },
          {
            title: "100% COMPATIBLE (ORDINATEUR, TABLETTE, SMARTPHONE) :",
            advantage:
                "L'application a été conçu pour être entièrement responsive. Chaque utilisateur " +
                "peut accéder à Apidae quel que soit son lieu de travail et depuis n'importe " +
                "qu'elle interface."
          }
        ]
      };
    }
  };
</script>

<style scoped>
  .advantage-container {
    padding-top: 8em;
  }

  .main-advantage {
    text-align: justify;
    margin-left: 10%;
    margin-bottom: 8em;
    width: 80%;
  }

  .advantage {
    font-size: large;
  }

  .place-button {
    bottom: 0;
    position: absolute;
    left: 50%;
  }

  .btn-yellow {
    position: relative;
    left: -50%;
    margin-top: 2em;
    margin-bottom: 2.2em;
    font-weight: bold;
    font-size: x-large;
    background-color: #fcce21;
  }

  .main-text {
    font-size: x-large;
  }

  .title-advantage {
    text-align: left;
    font-size: 3.6em;
  }
</style>
