<template>
  <Headers msg="WIGIF"/>
    <div class="uk-dark uk-padding uk-panel" style="text-align: center">
        <h1 class="uk-heading-line uk-text-center"><span>Contact</span></h1>
    </div>
    <div class="uk-text-center">
        <div class="uk-inline-clip uk-transition-toggle" tabindex="0">
        
            <img src="Transparent_Logo.svg" width="600" height="400" alt="" uk-scrollspy="cls: uk-animation-kenburns; repeat: true">
            <div class="uk-transition-fade uk-position-cover uk-position-small uk-overlay uk-overlay-primary uk-flex uk-flex-center uk-flex-middle">
                
                <div class="uk-grid-divider uk-child-width-expand@s" uk-grid style="text-align: center">
                    <p>Email : <br><br>Siège Social : </p>
                    <p><a href="mailto:wigif@protonmail.com">wigif@protonmail.com</a><br><br>Ecole d'Ingénieur ENSIBS <br> 17 bd Flandres Dunkerque 56321 LORIENT</p>
                </div>
            </div>
        </div>
    </div>

    <div class="uk-text-center uk-align-center uk-width-1-2@m" uk-grid>
        <div class="uk-card uk-card-secondary uk-card-body">
            <div class="uk-grid-divider uk-child-width-expand@s" uk-grid style="text-align: center">
                <p>Email : <br><br>Siège Social : </p>
                <p><a href="mailto:wigif@protonmail.com">wigif@protonmail.com</a><br><br>Ecole d'Ingénieur ENSIBS <br> 17 bd Flandres Dunkerque 56321 LORIENT</p>
            </div>
        </div>
    </div>

    <br>
    <div class="uk-background-secondary uk-light uk-padding uk-panel" style="text-align: center">©WIGIF</div>
</template>

<script>
import Headers from '../components/Headers.vue'

export default {
	name: "WIGIF",
	components: {
		Headers
	}
}
</script>