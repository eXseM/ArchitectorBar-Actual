<template>
    <div class="contacts">
        <!-- <content-page /> -->
        <content-v /> 
    </div>
</template>

<script>

// import contentPage from '~/components/contacts/content.vue'
import contentV from '~/components/contacts/contentV.vue'

    export default {
        components:{
            contentV
        }
    }
</script>

<style lang="scss" scoped>

// @import 'styles/shortcodes.css';
// @import 'styles/style.css';

.contacts{
    overflow: hidden;
    position: relative;
    background-color: #eeeeed;
}

</style>