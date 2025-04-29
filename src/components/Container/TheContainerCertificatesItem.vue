<script>
export default {
    name: 'TheContainerCertificatesItem',
    props: {
        title: {
            type: String,
            requierd: true,

        },
        company: {
            type: String,
            requierd: true,

        },
        date: {
            type: String,
            requierd: true,

        },
        icon: {
            type: String,
            requierd: true,

        }
    }
}
</script>

<template>
    <div class="certificates-item">
        <div class="certificates-info">
            <img :src="icon" class="certificates-icon" />
            <div>
                <div class="certificates-company">{{  company }}</div>
                <div class="certificates-title">{{  title }}</div>
            </div>

        </div>
        <div class="certificates-date">
            {{ date }}
        </div>
    </div>
</template>

<style scoped>
.certificates-item {
    display: flex;
    justify-content: space-between;
    padding: 32px;
    width: 100%;
}
.certificates-info {
    display: flex;
    gap: 16px;
    text-align: left;
}
.certificates-icon {
    border-radius: 10px;
    width: 43px;
    height: 43px;
    }
    .certificates-company {
        font-family: var(--font-family);
        font-weight: 400;
        font-size: 13px;
        line-height: 129%;
        letter-spacing: 0.01em;
        color: #79819a;
    }
    .certificates-title {
        font-family: var(--font-family);
        font-weight: 500;
        font-size: 15px;
        line-height: 125%;
        color: #2e2e48;
    }
    .certificates-date{
        font-family: var(--font-family);
        font-weight: 400;
        font-size: 11px;
        line-height: 133%;
        letter-spacing: 0.01em;
        color: #47516b;
    }

    @media (max-width: 500px) {
        .certificates-item {
    padding: 16px;
}
.certificates-title {
    font-size: 14px;
}
    }

</style>