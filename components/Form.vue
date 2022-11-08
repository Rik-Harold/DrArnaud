<template>
  <div class="formulaire">
    <input type="text" v-model="nom" />
    <input type="text" v-model="prenom" />
    <input type="text" v-model="objet" />
    <input type="text" v-model="message" />
    <!-- <Mailto :mail="email" :subject="objet" :body="message + '\n\n' + nom + ' ' + prenom" title="envoyer">
        <button>Envoyer</button>
    </Mailto> -->
    <Mailto
      :mail="email"
      :subject="objet"
      :body="message + '\n\n' + nom + ' ' + prenom"
      title="envoyer"
    />/
  </div>
</template>

<script>
export default {
  name: "FormVue",
  data() {
    return {
      email: "dndiaye389@gmail.com",
      nom: "",
      prenom: "",
      objet: "",
      message: "",
    };
  },
};
</script>

<style>
</style>
