<template>
  <Headers msg="WIGIF"/>
  <div class="uk-dark uk-padding uk-panel" style="text-align: center">
			<h1 class="uk-heading-line uk-text-center"><span>Prochain Workshop</span></h1>
		</div>
		<div class="uk-gridsmall uk-child-width-auto uk-flex uk-flex-center" uk-grid uk-countdown="date: 2022-01-26T18:00">
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
		<div class="uk-dark uk-padding uk-panel" style="text-align: center">
			<h1 class="uk-heading-line uk-text-center"><span>A Venir</span></h1>
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