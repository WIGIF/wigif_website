<template>
    <div class="list-subject">
        <li><button class="uk-button uk-button-text" uk-toggle="target: #modal-example" @click="popup">{{ label }}</button></li>
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
        }
    },
    methods: {
        popup() {
            this.$emit('receive', {message: this.label, option: this.text, link: this.link})
        }
    }
}
</script>