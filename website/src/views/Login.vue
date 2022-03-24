<template>
  <Headers msg="WIGIF"/>

	<div class="uk-align-center uk-width-1-2@m uk-position-center">
        <div class="uk-card uk-card-default uk-card-large uk-card-body">
            <h3 class="uk-card-title uk-text-center">Login</h3>
            <form class="uk-form">
				<div style="display: flex;justify-content: center;">
					<div class="uk-margin">
						<div class="uk-inline">
							<span class="uk-form-icon" uk-icon="icon: user"></span>
							<input class="uk-input" type="text">
						</div>
					</div>
				</div>	
				<div style="display: flex;justify-content: center;">
						<div class="uk-inline">
							<span class="uk-form-icon uk-form-icon-flip" uk-icon="icon: lock"></span>
							<input class="uk-input" type="text">
						</div>
				</div>
			</form>
			<button class="uk-button uk-button-default uk-align-center">Connexion</button>
			<p class="uk-text-center">Si vous n'avez pas encore de compte, veuillez-vous rapprocher de membres de l'assocation.</p>
        </div>
    </div>

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
