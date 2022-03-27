<template>
  <Headers msg="WIGIF"/>

	<div class="uk-align-center uk-width-1-2@m">
        <div class="uk-card uk-card-secondary uk-card-large uk-card-body">
            <h3 class="uk-card-title uk-text-center">Login</h3>
            <form class="uk-form">
				<div style="display: flex;justify-content: center;">
					<div class="uk-margin">
						<div class="uk-inline">
							<span class="uk-form-icon" uk-icon="icon: user"></span>
							<input class="uk-input" type="text" id="user">
						</div>
					</div>
				</div>	
				<div style="display: flex;justify-content: center;">
						<div class="uk-inline">
							<button class="uk-form-icon uk-form-icon-flip" uk-icon="icon: lock" type="password" @click="switchVisible"></button>
							<input :type="passwordFieldType" v-model="password" class="uk-input">
						</div>
				</div>
			</form>
			<button class="uk-button uk-button-default uk-align-center" v-on:click="showAlert">Connexion</button>
			<p class="uk-text-center">Si vous n'avez pas encore de compte, veuillez-vous rapprocher de membres de l'assocation.</p>
        </div>
    </div>

</template>

<script>
import Headers from '../components/Headers.vue'
import UIkit from '../uikit-webpack/node_modules/uikit';

export default {
	name: "WIGIF",
	components: {
		Headers
	},
	data () {
		return{
			password: "",
			passwordFieldType: "password"
		}
	},
	methods:{
		showAlert(){
			if(document.getElementById('user').value == "admin"){
				UIkit.notification({message: 'AHAH !! Votre tentative d\'intrusion a été enregistrée'})
			}
			else if(document.getElementById('user').value == "starf"){
				UIkit.notification({message : 'STARF'})
			}
			else{
				UIkit.notification({message: 'ALERT : Erreur de Login'})
			}
		},
		switchVisible(){
			this.passwordFieldType = this.passwordFieldType === "password" ? "text" : "password";
		}
	}
}
</script>
