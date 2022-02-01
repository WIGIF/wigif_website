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
                :key="item.label"></ListSubject>
            </ul>
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
            link1: ''
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
    }
}
</script>