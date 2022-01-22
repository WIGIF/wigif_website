<template>
  <Headers msg="WIGIF"/>
  <h1 class="uk-heading-medium uk-flex uk-flex-center">Les H@ck3rs de Kalité</h1>
  <p style="text-align: center">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  <div class="uk-grid-divider uk-child-width-expand@s" uk-grid>
    <div>
      <div class="uk-dark uk-padding uk-panel" style="text-align: center">
        <h1 class="uk-heading-line uk-text-center"><span>Workshop A Venir</span></h1>
      </div>
      <ul class="uk-list uk-list-striped" style="text-align: center">
        <ListSubject 
          v-for="item in newSubject" 
          :label="item.label"
          :text="item.text"
          :link="item.link"
          :key="item.label" 
          @click="displayPopUp"></ListSubject>
      </ul>
    </div>
    <div>
      <div class="uk-dark uk-padding uk-panel" style="text-align: center">
        <h1 class="uk-heading-line uk-text-center"><span>Historique Workshop</span></h1>
      </div>
      <ul class="uk-list uk-list-striped" style="text-align: center">
        <ListSubject 
          v-for="item in lastSubject" 
          :label="item.label"
          :text="item.text"
          :link="item.link"
          :key="item.label"
          @click="displayPopUp"></ListSubject>
      </ul>
    </div>
    <div id="modal-example" uk-modal>
        <div class="uk-modal-dialog uk-modal-body">
            <button class="uk-modal-close-default" type="button" uk-close></button>
            <h2 class="uk-modal-title">{{ label1 }}</h2>
            <p>{{ text1 }}</p><br>
            <a class="uk-link-text" :href="link1">Ressource Associée</a>
        </div>
      </div>
  </div><br><br>
  <div class="uk-background-secondary uk-light uk-padding uk-panel" style="text-align: center"></div>
</template>

<script>
import Headers from '../components/Headers.vue'
import ListSubject from '../components/ListSubject.vue'

export default {
	name: "WIGIF",
	components: {
		Headers,
    ListSubject
	},
  data () {
    return {
      label1: '',
      text1: '',
      link1: '',
      count: 1,
      newSubject: [{
        label: 'Coder de la Musique 🎶',
        text: 'Découverte d\'un logiciel permettant de coder de la Musique.'
      },
      {
        label: 'Assembleur II 💻',
        text: 'AA'
      },
      {
        label: 'Cryptographie I 🔑',
        text: 'AA'
      },
      {
        label: 'Découvrir BurpSuite 👨‍💻',
        text: 'AA'
      }],
      lastSubject: [ {
        label:'Outils de Bases sous Kali ⚙',
        link: "OUTILS_SOUS_KALI.pdf",
        text: 'Présentation de diverses outils utiles sous Kali (Nmap, Legion, Dirbuster, Binwalk, Exif, JohnTheRipper, ...). Afin de se familiariser avec ces outils et l\'environnement de Kali Linux, une petit box home-made a ensuite été effectuée.'
      }, 
      {
        label:'Assembleur I 💻',
        link: "Bases_des_Bases_Assembly.pdf",
        text: 'Premier cours d\'introduction à l\'assembleur. Au programme : Explication du fonctionnement de la mémoire dans un ordinateur - Explication du passage d\'un code lisible par l\'homme à un code lisible par l\'ordinateur - Découverte des instructions en Assembleur - Premier Exercice avec le logiciel Cutter'
      },
      {
        label:'Découvrir GIT 📁',
        text: 'AA'
      }]
    }
  },
  methods: {
    displayPopUp(payload) {
      this.count ++
      var remain = this.count % 2
      if(Math.floor(remain >= 0 ? remain : remain + 2) === 0){ //Opération Modulo en Javascript
        this.label1 = payload.message,
        this.text1 = payload.option,
        this.link1 = payload.link,
        console.log("POP UP" + payload.message + payload.option)
      }
    }
  }
}
</script>
