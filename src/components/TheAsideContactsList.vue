<script>
import TheAsideContactsListItem from './TheAsideContactsListItem.vue';

export default {
    name: 'TheAsideContactsList',
    components: {
        TheAsideContactsListItem
    },
    props: {
        contacts: {
            type: Array,
        }
    }
}
</script>

<template>
    <ul>
        <TheAsideContactsListItem
            v-for="contact in contacts"
            :key="contact.id"
            :icon="contact.icon"
            :title="contact.title"
            :text="contact.text"
        />
    </ul>
</template>