<script>
export default {
    name: 'TheAsideContactsListItem',
    props: {
        icon: {
                type: String,
                required: true
        },
        title: {
                type: String,
                required: true
        },
        text: {
                type: String,
                required: true
        }
    },
    computed: {
        isEmail() {
            return this.text.includes('@');
        },
        isPhone() {
            return this.title.toLowerCase().includes('phone');
        }
    }
}
</script>


<template>
    <div class="aside-contacts-list-item">
        <div class="aside-contacts-list-item-icon">
            <slot name="icon"><img :src="icon" /></slot>
        </div>
        <div class="aside-contacts-list-item-info">
            <div class="aside-contacts-list-item-title">
                <slot name="title">{{ title }}</slot>
            </div>
            <div class="aside-contacts-list-item-text">
                <a 
                    v-if="isEmail"
                    :href="`mailto:${text}`"
                    >{{ text }}</a>
                <a v-else-if="isPhone"
                    :href="`tel:${text}`"
                    >{{ text }}</a>
                <span v-else> {{ text }}</span>
            </div>
        </div>
    </div>

</template>

<style scoped>
.aside-contacts-list-item {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 16px;
}
.aside-contacts-list-item-icon {
    width: 32px;
    height: 32px;
}
.aside-contacts-list-item-title {
    font-weight: 400;
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    padding-bottom: 4px;
}
.aside-contacts-list-item-text {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #47516b;
}

</style>