<template>
  <div class="div-contact">
    <Cardtitle
      titre="ME CONTACTER"
      class="pb-4 text-center"
      position="margin-left:-22.3vw;margin-top:5vw;width:61.2%"
    />
    <div class="coordonne">
      <div class="form-group">
        <div class="col-12 name-mail">
          <input
            type="text"
            v-model="nom"
            name="nom"
            class="nom"
            placeholder="Nom"
          />

          <input
            type="email"
            v-model="email"
            name="email"
            class="mail"
            placeholder="Votre addresse email"
          />
        </div>

        <input
          type="text"
          name="objet"
          v-model="objet"
          class="objet"
          placeholder="Objet"
        />

        <textarea
          name="message"
          id=""
          v-model="message"
          class="textarea"
          cols="10"
          rows="10"
          placeholder="Message"
        >
        </textarea>

        <Mailto
          :mail="email"
          :subject="objet"
          :body="message + '\n\n' + nom"
          title="envoyer"
        >
          <!-- <button type="button" id="button" @click="send(instance)" class="form-control button">Envoyer</button> -->
          <button type="button" id="button" class="form-control button">
            Envoyer le mail
          </button>
        </Mailto>
        <!-- <Mailto :mail="destinataire" :subject="objet" :body="message + '\n\n' + nom" title="Envoyer">
                      <button type="button" @click="send(instance)" id="mailButton">
                          Envoyer
                      </button>
                    </Mailto> -->
      </div>

      <div class="col-lg-5 col-md-6 col-12 name-part">
        <h2 style="color: rgba(2, 56, 137, 1)">Dr Arnaud Yémalin ZANNOU</h2>
        <div class="reso">
          <Reseau
            id="Reseau"
            linkedin="width:3vw;height:2.5vw;margin-left:1vw;margin-top:-0.3vw;"
            mail="width:3.5vw;border: 1px solid transparent;height:2.2vw;margin-left:1.3vw"
            call="width:2.8vw;height:2.3vw;margin-left:1.3vw"
            numcol="color:rgba(2, 56, 137, 1);margin-left:1vw;font-size:1.8vw;font-weight: 600;font-family:Roboto,sans-serif"
          />
          <div class="resmob">
            <Resmobile />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import emailjs from 'emailjs-com';
import Reseau from "./Reseau.vue";
import Cardtitle from "./Cardtitle.vue";
import Resmobile from "./Resmobile.vue";
export default {
  name: "Contact",
  components: {
    Reseau,
    Cardtitle,
    Resmobile,
  },
  data() {
    return {
      instance: null,
      destinataire: "dndiaye389@gmail.com",
      nom: "Rik",
      objet: "",
      email: "",
      message: "Test de nuxt",
    };
  },
  mounted() {
    this.instance = this;
  },
  methods: {
    send: (instance) => {
      // Notification de mail envoyé
      alert(
        "Vous serez redirigé vers votre boite mail pour confirmer l'envoi du mail !"
      );
      // Initialisation
      setTimeout(() => {
        instance.nom = "";
        instance.objet = "";
        instance.message = "";
      }, 1500);
    },

    // send(instance ) {
    //   console.log(instance);
    //   alert('vous allez etre rediriger vers la boite mail')
    //   setTimeout(() => {
    //     instance.nom= ''
    //     instance.objet= ''
    //     instance.message= ''
    //   }, 1500);
    //   this.$mail.send({
    //     from:this.email,
    //     subject: 'Contact form message',
    //     text: this.message,
    //   })
    // }
  },
};
</script>
<style>
.coordonne {
  padding-left: 2%;
  display: flex;
  width: auto;
  padding-bottom: 3vw;
  background-color: rgba(255, 242, 238, 1);
}

.form-group {
  /* border: 1px solid black; */
  margin-left: 10%;
}

.form-group input,
textarea ::placeholder {
  font-family: "Montserrat-Regular";
  color: rgb(46, 44, 44);
}

.name-mail {
  display: inline-flex;
  padding-left: 0px;
  padding-right: 0%;
}

/* CASE MAIL  */
.name-mail .mail {
  width: 72%;
  margin-left: 4%;
  margin-top: 0vw;
}

/* NOM  */
.name-mail .nom {
  width: 45%;
}

textarea,
.objet,
.name-mail {
  width: 100%;
}

.textarea,
.objet {
  margin-top: 1vw;
}

.button {
  width: 100%;
  background: rgba(232, 96, 48, 1);
  font-size: 1.5vw;
  line-height: 1.4vw;
  letter-spacing: 0px;
  text-align: center;
  margin-top: 1vw;
}

#button {
  font-family: "Montserrat", sans-serif;
  font-weight: 700;
  color: white;
}

.nom,
.mail,
.objet,
.button {
  height: 2.9vw;
  border-radius: 0.4vw;
  border: 1px solid #cccccc;
}

.textarea {
  border-radius: 0.4vw;
  border: 1px solid rgb(223, 216, 216);
}

.nom:focus,
.mail:focus,
.objet:focus,
textarea:focus {
  outline: 1px solid rgba(232, 96, 48, 1);
  font-size: 1vw;
  color: rgb(7, 7, 29);
}

::placeholder {
  color: #9b9b9b;
  opacity: 1;
  /* Firefox */
  font-family: "Montserrat";
  padding-top: 0.89vw;
  padding-left: 1vw;
  font-weight: 400;
  font-size: 1.1vw;
  line-height: 1.4vw;
  letter-spacing: 0px;
  text-align: left;
}

:-webkit-input-placeholder {
  /* Chrome, Safari, Opera */
  color: #cccccc;
}

::-ms-input-placeholder {
  /* Microsoft Edge */
  color: #cccccc;
}

form {
  margin-left: auto;
  padding-top: 8vw;
  padding-bottom: 6.4vw;
  width: 36vw;
}

/* ******Partie des adresses********** */
.name-part {
  margin-left: 6%;
}

.name-part h2 {
  margin-top: 50%;
  font-family: "Roboto", sans-serif;
  font-weight: 600;
  font-size: 2vw;
}

.reso {
  width: 100%;
  height: auto;
  padding-left: 4%;
  padding-top: 01vw;
}

.resmob {
  display: none;
}

@media screen and (max-width: 768px) {
  .nom,
  .mail,
  .objet,
  .button {
    height: 8.5vw;
    border-radius: 1vw;
  }

  .textarea {
    border-radius: 1vw;
    height: 32vw;
  }
  .nom:focus,
  .mail:focus,
  .objet:focus,
  textarea:focus {
    outline: 1px solid rgba(232, 96, 48, 1);
    font-size: 4vw;
    color: rgb(7, 7, 29);
  }

  .textarea,
  .objet {
    margin-top: 2vw;
  }

  .button {
    margin-top: 2vw;
    font-size: 4.1vw;
  }

  ::placeholder {
    padding-top: 2vw;
    font-size: 4.1vw;
    line-height: 1.4vw;
  }

  .form-group {
    width: 78vw;
  }
  .form-group input {
    font-size: 4vw;
    padding: 2vw 2vw;
  }
  .coordonne {
    padding-left: 2%;
    flex-direction: column;
    width: auto;
  }

  .name-part {
    margin-left: 6%;
    padding-left: 4vw;
    background-color: rgba(255, 242, 238, 1);
  }

  .name-part h2 {
    margin-top: 6%;
    font-size: 6vw;
  }

  .reso {
    width: auto;
    height: auto;
  }

  #Reseau {
    display: none;
  }

  .resmob {
    display: block;
  }
}
</style>