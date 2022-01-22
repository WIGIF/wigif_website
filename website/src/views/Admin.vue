<template>
  <Headers msg="WIGIF"/>
  <div class="uk-dark uk-padding uk-panel" style="text-align: center">
    <h1 class="uk-heading-line uk-text-center"><span>Tableau de Bord : {{ $route.params.id }}</span></h1>
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
