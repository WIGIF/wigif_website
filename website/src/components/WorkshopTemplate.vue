<template>
    <div class="workshop-template">
        <div>
            <div class="uk-dark uk-padding uk-panel" style="text-align: center">
                <h1 class="uk-heading-line uk-text-center"><span>{{ title }}</span></h1>
            </div>
            <ul class="uk-list uk-list-striped" style="text-align: center">
            <ListSubject 
                v-for="item in listWork" 
                :label="item.label"
                :text="item.text"
                :link="item.link"
                :key="item.label" 
                @receive="displayPopUp"></ListSubject>
            </ul>
        </div>
        <div id="modal-example" uk-modal>
            <div class="uk-modal-dialog uk-modal-body">
                <button class="uk-modal-close-default" type="button" uk-close></button>
                <h2 class="uk-modal-title">{{ label1 }}</h2>
                <p>{{ text1 }}</p><br>
                <a class="uk-link-text" :href="link1">Ressource Associée</a>
            </div>
        </div>
    </div>
</template>

<script>
import ListSubject from '../components/ListSubject.vue'

export default {
    name: 'WorkshopTemplate',
    components: {
        ListSubject
	},
    data (){
        return {
            label1: '',
            text1: '',
            link1: '',
            //count: 1
        }
    },
    props: {
        title: {
            type: String,
            required: true
        },
        listWork: {
            type: Array,
            required: true
        }
    },
    methods: {
        displayPopUp(payload) {
            //this.count ++
            //var remain = this.count % 2
            //if(Math.floor(remain >= 0 ? remain : remain + 2) === 0){ //Opération Modulo en Javascript
            this.label1 = payload.message,
            this.text1 = payload.option,
            this.link1 = payload.link,
            console.log("POP UP" + payload.message + payload.option + this.label1)
            //}
        }
    }  
}
</script>