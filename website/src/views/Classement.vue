<template>
<Headers msg="WIGIF"/>
<div>
<div class="uk-dark uk-padding uk-panel" style="text-align: center">
        <h1 class="uk-heading-line uk-text-center"><span>Classement Root-Me</span></h1>
	</div>
    <table class="uk-table uk-table-striped uk-text-center">
        <thead>
            <tr>
                <th class="uk-text-center">Rang Local</th>
                <th class="uk-text-center">Pseudo</th>
                <th class="uk-text-center">Points</th>
                <th class="uk-text-center">Rang Global</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>RvSupTo</td>
                <td>1 805 pts</td>
                <td>4 564 ème</td>
            </tr>
        </tbody>
    </table>
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
