<script>
export default {
    name: 'TheContainerProjectsItem',
    props: {
        title: {
            type: String,
        },
        subtitle: {
            type: String,
        },
        icon: {
            type: String,
        },
        link: {
            type: String,
        }
    }
}
</script>

<template>
    <div>
    <div class="project-item">
        <img :src="icon" :alt="title" class="project-icon" />
        <div>
            <div class="project-title">{{ title }}</div>
            <div class="project-subtitle">{{ subtitle }}</div>
        </div>     
    </div>
    <div class="project-link-wrapper"><img src="/svg/link.svg" alt="Link"/><a class="project-link">{{ link }}</a></div>
</div>
</template>

<style scoped>
.project-item {
    display: flex;
    align-items: center;
    text-align: left;
    gap: 16px;
    margin-bottom: 10px;
}
    .project-icon {
        border-radius: 8px;
        width: 48px;
        height: auto;
    }
    .project-title {
        font-family: var(--font-family);
        font-weight: 500;
        font-size: 16px;
        line-height: 125%;
        color: #2e2e48;
    }
    .project-subtitle {
        font-family: var(--font-family);
        font-weight: 400;
        font-size: 14px;
        line-height: 129%;
        letter-spacing: 0.01em;
        color: #79819a;
    }
    .project-link {
        font-family: var(--second-family);
        font-weight: 600;
        font-size: 16px;
        line-height: 125%;
        text-decoration: underline;
        text-decoration-skip-ink: none;
        color: #516cf7;
    }
    .project-link-wrapper {
        display: flex;
        gap: 5px;
        align-items: center;
    }


</style>