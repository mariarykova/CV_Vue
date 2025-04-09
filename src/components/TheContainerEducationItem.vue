<script>
export default {
    name: 'TheContainerEducationItem',
    props: {
        name: {
            type: String,
        },
        degree: {
            type: String,
        },
        date: {
            type: String,
        },
        icon: {
            type: String,
        }
    }
}
</script>

<template>
    <div class="education-item">
        <div class="education-info">
            <img :src="icon" class="education-icon" />
            <div class="education-name">{{ name }}</div>
        </div>
        <div class="education-degree">{{ degree }}</div>
        <div class="education-date">{{ date }}</div>
    </div>
</template>

<style scoped>
.education-item {
    display: flex;
    flex-direction: column;
    padding: 32px;
    text-align: start;
}
.education-info {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 16px;
}
.education-icon {
    width: 38px;
    height: 48px;
}
.education-name {
    font-family: var(--font-family);
    font-weight: 500;
    font-size: 12px;
    line-height: 133%;
    color: #2e2e48;
}
.education-degree {
    font-family: var(--font-family);
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #2e2e48;
    width: 100%;
    max-width: 178px;
}
.education-date {
    font-family: var(--font-family);
    font-weight: 400;
    font-size: 10px;
    letter-spacing: 0.01em;
    color: #79819a;
}


</style>