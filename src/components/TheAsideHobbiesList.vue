<script>
import BaseItemLayout from './BaseItemLayout.vue';

export default {
    name: 'TheAsideLanguagesList',
    components: {
        BaseItemLayout
    },
    props: {
        hobbies: {
            type: Array,
        }
    }
}
</script>

<template>
    <ul>
        <BaseItemLayout
            v-for="hobby in hobbies"
            :key="hobby.id"
            :icon="hobby.icon"
            :title="hobby.title"
            :text="hobby.text"
        />
    </ul>
</template>