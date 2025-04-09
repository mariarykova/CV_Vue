<script>
import BaseItemLayout from './BaseItemLayout.vue';

export default {
    name: 'TheAsideContactsList',
    components: {
        BaseItemLayout
    },
    props: {
        socials: {
            type: Array,
        }
    }
}
</script>

<template>
    <ul>
        <BaseItemLayout
            v-for="social in socials"
            :key="social.id"
            :icon="social.icon"
            :title="social.title"
            :text="social.text"
        />
    </ul>
</template>