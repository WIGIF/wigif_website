<template>
    <div class="headers">
        <div class="uk-background-secondary uk-light uk-padding uk-panel" style="text-align: center">
            <table class="uk-table uk-table-justify uk-table-divider">
            <tbody>
                <tr>
                    <td class="uk-width-small"><button class="uk-button uk-button-default uk-margin-small-left" type="button" uk-toggle="target: #offcanvas-push"><span uk-icon="menu"></span></button></td>
                    <td><h1 class="uk-heading-line uk-text-center"><span>{{ msg }}</span></h1></td>
                    <td class="uk-width-small"><router-link to="/login"><button class="uk-button uk-button-default uk-margin-small-right" type="button"><span uk-icon="user"></span></button></router-link></td>
                </tr>
            </tbody>
            </table>
        </div>
        <div id="offcanvas-push" uk-offcanvas="mode: push; overlay: true">
            <div class="uk-offcanvas-bar uk-flex uk-flex-column">
                    <button class="uk-offcanvas-close" type="button" uk-close></button>
                    <ul class="uk-nav uk-nav-primary uk-nav-center uk-margin-auto-vertical">
                        <li><router-link to="/">Accueil</router-link></li>
                        <li><router-link to="/classement">Classement & CTFs</router-link></li>
                        <li><router-link to="/news">News</router-link></li>
                        <li><router-link to="/agenda">Agenda</router-link></li>
                        <li><router-link to="/workshop">Workshop</router-link></li> 
                        <li><router-link to="/contact">Contact</router-link></li> 
                    </ul>
            </div>
        </div>
        
    </div>
</template>

<script>
export default {
  name: 'Headers',
  props: {
    msg: String
  }
}
</script>