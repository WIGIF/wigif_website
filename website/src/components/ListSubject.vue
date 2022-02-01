<template>
    <div class="list-subject">
        <li><button class="uk-button uk-button-text" :uk-toggle="target">{{ label }}</button></li>
    </div>
    <div :id="id" uk-modal>
      <div class="uk-modal-dialog uk-modal-body">
        <button class="uk-modal-close-default" type="button" uk-close></button>
        <h2 class="uk-modal-title">{{ label }}</h2>
        <p>{{ text }}</p><br>
        <a class="uk-link-text" :href="link">Ressource Associée</a>
      </div>
    </div>
</template>

<script>
export default {
    name: 'ListSubject',
    props: {
        label: {
            type: String,
			required: true
        },
        text: {
            type: String,
            required: true
        },
        link: {
            type: String
        },
    },
    data(){
        return{
            id : "modal-example-"+this.label.toLowerCase().split(" ").join(""),
            target : "target: #modal-example-"+this.label.toLowerCase().split(" ").join("")
        }
    }
}
</script>