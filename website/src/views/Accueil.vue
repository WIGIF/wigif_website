<template>
  <Headers msg="WIGIF"/>

  <h1 class="uk-heading-medium uk-flex uk-flex-center">Les H@ck3rs de Kalité</h1>
  <p style="text-align: center">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  
  <div class="uk-grid-divider uk-child-width-expand@s" uk-grid>
    <WorkshopTemplate :listWork="newSubject" title="Workshop A Venir"/>
    <WorkshopTemplate :listWork="lastSubject" title="Historique Workshop"/>
  </div>
  <br><br>
  <div class="uk-background-secondary uk-light uk-padding uk-panel" style="text-align: center"></div>
</template>

<script>
import Headers from '../components/Headers.vue'
import WorkshopTemplate from '../components/WorkshopTemplate.vue'

export default {
	name: "WIGIF",
	components: {
		Headers,
    WorkshopTemplate
	},
  data () {
    return {
      newSubject: [{
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
      },
      {
        label: 'Coder de la Musique 🎶',
        text: 'Découverte d\'un logiciel permettant de coder de la Musique.'
      }]
		}
	},
	methods: {
    refresh() {
      this.$router.go()
    }
  } 
}
</script>
