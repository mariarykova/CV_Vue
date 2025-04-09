
<script>
import TheContainerCertificatesItem from './TheContainerCertificatesItem.vue';

export default {
    name: 'TheContainerCertificates',
    components: { TheContainerCertificatesItem },
    data() {
        return {
        certificates: [
        {
            id: 1,
            title: 'Frontend in Computer Science',
            company: 'Kobezzza Lab',
            date: 'March 2023 - Oct 2023',
            icon: "/svg/kobezzza.svg",
        }
    ]
        }
    }
    
};
</script>

<template>
        <div class="component-title"><div class="spot-tick"></div>Certificates & Awards</div>
        <div class="certificates-list">
            <div class="divider"></div>
            <TheContainerCertificatesItem
            v-for="certificate in certificates"
            :key="certificate.id"
            :title="certificate.title"
            :company="certificate.company"
            :date="certificate.date"
            :icon="certificate.icon"
        />
        </div>
</template>

<style scoped>
.certificates-list {
    display: flex;
    margin-left: 2px;
}
</style>