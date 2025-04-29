<script>
import BaseItemLayout from '../Base/BaseItemLayout.vue';

export default {
    name: 'TheAsideLanguagesList',
    components: {
        BaseItemLayout
    },
    props: {
        languages: {
            type: Array,
            required: true
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