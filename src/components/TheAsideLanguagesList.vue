<script>
import BaseItemLayout from './BaseItemLayout.vue';

export default {
    name: 'TheAsideLanguagesList',
    components: {
        BaseItemLayout
    },
    props: {
        languages: {
            type: Array,
        }
    }
}
</script>

<template>
    <ul>
        <BaseItemLayout
            v-for="language in languages"
            :key="language.id"
            :icon="language.icon"
            :title="language.title"
            :text="language.text"
        />
    </ul>
</template>