<template>
  <div class="solution-container">
    <h2 class="title-solution">Nos solutions RH Apidae</h2>
    <hr class="split-line"/>
    <section id="solutions" class="row">
      <feature v-for="feature in features" :illustration="feature.illustration" :id="feature.id" :key="feature.id" :link="feature.reference"
         class=" col-xs-12 col-lg-3 col-md-6 feature_container">
        <span class="title" slot="title">{{feature.title}}</span>
        <span class="subtitle" slot="subtitle">{{feature.subtitle}}</span>
        <p class="description" slot="description">{{feature.description}}</p>
        <p class="description" slot="description2">{{feature.description2}}</p>
        <p class="description" slot="description3">{{feature.description3}}</p>
        <a class="btn learn-more" slot="button" v-bind:href="feature.reference">{{feature.label}}</a>
      </feature>
    </section>
  </div>
</template>
<script type="text/ecmascript-6">
  import Feature from "./feature";

  export default {
    components: {
      Feature
    },
    data () {
      return {
        features: [
          {
            id: "suivi-d’activité",
            title: "Suivi d’activité",
            illustration: "fa fa-3x fa-line-chart color-illustration",
            subtitle: "Gain de temps, plus d'oubli",
            description:
                "C'est l'heure du bilan d'activité mensuel.",
            description2:
                "L'un de vos collaborateurs ne se rappelle plus ce qu'il a fait le vendredi 12 après-midi ?",
            description3:
                "Plus de prise de tête : les tâches peuvent être saisies au jour le jour en toute simplicité. Coté manager, vous avez une vision globale du planning et de l'organisation de vos équipes.",
            label: "En savoir plus",
            reference: "cra"
          },
          {
            id: "congés-et-absences",
            title: "Congés et absences",
            illustration: "fa fa-3x fa-plane color-illustration",
            subtitle: "Rapide, simple et efficace",
            description:
                "En quelques clics, les collaborateurs posent leurs prévisions de congés ou renseignent leurs absence (RTT, déplacements ...). Ils reçoivent la réponse par email dès que le manager a répondu.",
            description2:
                "Dès la validation, les périodes concernées sont automatiquement renseignées dans le rapport d'activité du collaborateur heureux qui va partir en vacances.",
            description3:
                "Le calendrier global des absences vos permet de visualiser mois par mois le planning prévu.",
            label: "En savoir plus",
            reference: "./src/absences.html"
          },
          {
            id: "notes-de-frais",
            title: "Notes de frais",
            illustration: "fa fa-3x fa-credit-card color-illustration",
            subtitle: "Fini la paperasse inutile",
            description:
                "A la fin du repas avec le client, et depuis son smartphone, le collaborateur crée et vous envoie la note de frais en quelques clics. ",
            description2:
                "Plus besoin de rechercher les justificatifs égarés ou rangés au fond d'un tiroir.",
            description3:
                "De votre coté, vous optimisez le délai de remboursement et avez une vision globale des frais liés à chacun des services de l'entreprise.",
            label: "En savoir plus",
            reference: "./src/frais.html"
          },
          {
            id: "time-tracking",
            title: "Time tracking",
            illustration: "fa fa-3x fa-clock-o color-illustration",
            subtitle: "Traçabilité des tâches à venir ou en cours",
            description:
                "Suivez en temps réel les temps d'activité de chacun de vos collaborateurs, par tâche et par projet, et obtenez des synthèses significatives et détaillées. ",
            description2:
                "Idéal pour l'organisation du travail et pour disposer d'une vue globale de l'activité de chacun des membres de votre équipe. Le collaborateur, lors d'une nouvelle tâche sur un projet, peut déclencher un chronomètre en début d'activité, et l'arrêter selon ses besoins ou contraintes, ou bien tout simplement lorsque la tâche est terminée.",
            description3:
                "",
            label: "En savoir plus",
            reference: "./src/time.html"
          }
        ]
      };
    },

    methods: {
      scroll_to_signup: function () {
        $("html, body").animate(
          {
            scrollTop: $("#signup-form").offset().top
          },
          1000
        );
      }
    }
  };
</script>

<style>
  .solution-container{
    padding-top: 8em;
    text-align: center;
  }

  .title-solution {
    font-size: 3.6em;
  }

  .split-line {
    margin-left: 10%;
    width: 80%;
  }

  .feature_container{
    font-weight: bold;
    font-size: large;
    padding: 0;
    padding-bottom: 4em;
  }

  .color-illustration {
    color: #fcce21;
    border-bottom: black solid 1px;
    width: 100%;
    padding-bottom: 1.2em;
  }

  #solutions{
    top: 10vh;
    margin: 3em 0  0 0;
  }

  .learn-more {
    background-color: #fcce21;
    font-size: large;
    font-weight: bold;
    position: relative;
    left: -50%;
  }

</style>
