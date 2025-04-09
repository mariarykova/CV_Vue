<script>
export default {
    name: 'TheContainerSkillsItem',
    props: {
        title: {
            type: String,
        },
        subtitle: {
            type: String,
        },
        icon: {
            type: String,
        }
    }
}
</script>

<template>
    <div>
        <img :src="icon" :alt="title" class="skill-icon" />
        <div class="skill-title">{{ title }}</div>
        <div class="skill-subtitle">{{ subtitle }}</div>
    </div>

</template>

<style scoped>
    .skill-icon {
        border-radius: 8px;
        width: 48px;
        height: auto;
    }
    .skill-title {
        font-family: var(--font-family);
        font-weight: 500;
        font-size: 14px;
        line-height: 129%;
        color: #2e2e48;
    }
    .skill-subtitle {
        font-family: var(--font-family);
        font-weight: 400;
        font-size: 10px;
        letter-spacing: 0.01em;
        text-align: center;
        color: #79819a;
    }


</style>