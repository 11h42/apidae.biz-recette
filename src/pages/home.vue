<template>
  <div>
    <cover :scroll_to_signup="scroll_to_signup" :is_with_video="true"
           :is_with_information="true" :is_main_title="true">
      <span slot="header" class="m-x-auto">
        Apidae : Solution de management des ressources
      </span>
      <small slot="header-subtitle">Apidae est le logiciel de management des ressources en entreprise idéal pour le
        TPE/PME.
        Vous allez pouvoir centraliser et automatiser des procédures administratives telle que la
        <b>gestion des notes de frais</b>, <b>la gestion des congés et des absneces</b> des salariés ainsi
        que la <b>gestion du suivi d'activité</b> au sein de l'entreprise. Des solutions RH dans une seule
        application, c'est ce que Apidae vous propose &nbsp;!
      </small>
      <small slot="text_button_free" class="size-btn-cover">
        <i class='fa fa-arrow-circle-o-right'/>&nbsp;Essayer gratuitement notre solution APIDAE !
      </small>
    </cover>

    <div class="container-fluid">
      <solution></solution>

      <advantage :showbtntry="true" :scroll_to_signup="scroll_to_signup"></advantage>

      <pricing :ascomponent="true" :scroll_to_signup="scroll_to_signup"></pricing>

      <signup :scroll_to_price="scroll_to_price"></signup>

      <section id="nous-contacter" class="row">
        <call-to-action class="col-xs-12"></call-to-action>
      </section>
    </div>
  </div>
</template>
<script type="text/ecmascript-6">
  import Cover from "../components/cover";
  import CallToAction from "../components/call-to-action";
  import Solution from "../components/solution";
  import Advantage from "../components/advantage";
  import Pricing from "../Pricing.vue";
  import Signup from "../Signup.vue";

  export default {
    components: {
      CallToAction,
      Solution,
      Advantage,
      Cover,
      Pricing,
      Signup
    },

    methods: {
      scroll_to_signup: function () {
        $("html, body").animate(
          {
            scrollTop: $("#signup-form").offset().top
          },
          1000
        );
      },
      scroll_to_price: function () {
        $("html, body").animate(
          {
            scrollTop: $("#pricing-form").offset().top
          },
          1000
        );
      }
    }
  };
</script>
