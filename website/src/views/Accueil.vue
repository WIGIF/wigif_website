<template>
  <Headers msg="WIGIF"/>

  <h1 class="uk-heading-medium uk-flex uk-flex-center">Les H@ck3rs de Kalité</h1>
  <p style="text-align: center">
  WIGIF (Where I Go I Flag) est une association étudiante qui a pour but de partager les bases de la cybersécurité aux étudiants du parcours préparatoire de l'ENSIBS (Ecole Nationale Supérieure d'Ingénieur Bretagne Sud)
. <br>Sur ce site vous pourrez trouvez les différents ateliers à venir et passés, les news de l'association, le classements Root-Me des membres de l'association, ainsi qu'un agenda des prochain CTFs (Capture The Flag). 
<br>~Keep Pwn </p>
  
  <div class="uk-grid-divider uk-child-width-expand@s" uk-grid>
    <WorkshopTemplate :listWork="newSubject" title="Workshop A Venir"/>
    <WorkshopTemplate :listWork="lastSubject" title="Historique Workshop"/>
  </div>
  <br><br>
  <div class="uk-background-secondary uk-light uk-padding uk-panel" style="text-align: center">©WIGIF</div>
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
        text: 'Prochainement !! Nous vous attendons avec impatience !!'
      },
      {
        label: 'Introduction aux injections SQL 💉',
        text: 'Prochainement !! Nous vous attendons avec impatience !!'
      },
      {
        label: 'Découvrir BurpSuite 👨‍💻',
        text: 'Prochainement !! Nous vous attendons avec impatience !!'
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
        text: 'Historique de GIT et découverte de Github.',
        link: 'gitdiapo.pdf'
      },
      {
        label: 'Coder de la Musique 🎶',
        text: 'Découverte d\'un logiciel permettant de coder de la Musique.'
      },
      {
        label: 'Présentation de Tic-Tools ⚙',
        text: 'Présentation des objectifs du projet Tick-Tools et proposition d\' idée d\'amélioration de l\'outil.'
      },
      {
        label: 'Cryptographie I 🔑',
        text: 'Première approche de la cryptographie via RSA. Découverte de la mécanique de chiffrement et Attaque par Factorisation de clés RSA.',
        link: 'Cryptanalyse_I.pdf'
      },
      ]
		}
	},
	methods: {
    refresh() {
      this.$router.go()
    }
  } 
}
</script>
