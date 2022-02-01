<template>
	<Headers msg="WIGIF"/>
	
	<div class="uk-dark uk-padding uk-panel" style="text-align: center">
		<h1 class="uk-heading-line uk-text-center"><span>Prochain Workshop</span></h1>
	</div>
	
	<div class="uk-gridsmall uk-child-width-auto uk-flex uk-flex-center" uk-grid uk-countdown="date: 2022-01-31T18:00">
		<div>
			<div class="uk-countdown-number uk-countdown-days"></div>
			<div class="uk-countdown-label uk-margin-small uk-text-center uk-visible@s">Days</div>
		</div>
		<div class="uk-countdown-separator">:</div>
		<div>
			<div class="uk-countdown-number uk-countdown-hours"></div>
			<div class="uk-countdown-label uk-margin-small uk-text-center uk-visible@s">Hours</div>
		</div>
		<div class="uk-countdown-separator">:</div>
		<div>
			<div class="uk-countdown-number uk-countdown-minutes"></div>
			<div class="uk-countdown-label uk-margin-small uk-text-center uk-visible@s">Minutes</div>
		</div>
		<div class="uk-countdown-separator">:</div>
		<div>
			<div class="uk-countdown-number uk-countdown-seconds"></div>
			<div class="uk-countdown-label uk-margin-small uk-text-center uk-visible@s">Seconds</div>
		</div>
	</div>
	
	<WorkshopTemplate :listWork="newSubject" title="Workshop A Venir"/>
	<WorkshopTemplate :listWork="lastSubject" title="Historique Workshop"/>

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
				text: 'AA',
				link: ''
			},
			{
				label: 'Cryptographie I 🔑',
				text: 'AA',
				link: ''
			},
			{
				label: 'Découvrir BurpSuite 👨‍💻',
				text: 'AA',
				link: ''
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
				text: 'AA',
				link: ''
			},
			{
				label: 'Coder de la Musique 🎶',
				text: 'Découverte d\'un logiciel permettant de coder de la Musique.',
				link: ''
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