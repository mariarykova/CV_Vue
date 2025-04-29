<script>
export default {
    name: 'BaseItemLayout',
    props: {
        icon: {
            type: String,
            requierd: true,
        },
        title: {
            type: String,
            requierd: true,
        },
        text: {
            type: String,
            requierd: true,
        }
    },
    computed: {
        isSocial() {
            return this.text.includes('@');
        }
    }
}
</script>


<template>
    <div class="base-item-layout">
        <div class="base-item-layout-icon">
            <slot name="icon"><img :src="icon" /></slot>
        </div>
        <div class="base-item-layout-info">
            <div class="base-item-layout-title">
                <slot name="title">{{ title }}</slot>
            </div>
            <div :class="['base-item-layout-text', { social: isSocial }]">
                <span>{{ text }}</span>
            </div>
        </div>
    </div>

</template>

<style scoped>
.base-item-layout {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 16px;
}
.base-item-layout-icon {
    width: 32px;
    height: 32px;
}
.base-item-layout-title {
    font-weight: 400;
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    padding-bottom: 4px;
}
.base-item-layout-text {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #47516b;
}
.social {
    text-decoration: underline;
    cursor: pointer;

}

</style>