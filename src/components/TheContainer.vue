<script>

import TheContainerExperience from './TheContainerExperience.vue';
import TheContainerSkills from './TheContainerSkills.vue';
import TheContainerProjects from './TheContainerProjects.vue';
import TheContainerCertificates from './TheContainerCertificates.vue';
import TheContainerEducation from './TheContainerEducation.vue';

export default {
    name: 'TheContainer',
    components: {
        TheContainerExperience,
        TheContainerSkills,
        TheContainerProjects,
        TheContainerCertificates,
        TheContainerEducation
    },
}

</script>

<template>
 <div class="main-container">
    <TheContainerEducation />
    <TheContainerExperience />
    <TheContainerSkills />
    <TheContainerProjects />
    <TheContainerCertificates />
 </div>
</template>

<style scoped>
.main-container {
    padding: 64px 48px 0px 32px;
    width: 100%;;
    max-width: 843px;
    background-color: #f7f9fc;
}

@media (max-width: 1025px) {
    .main-container {
    padding: 64px 25px 0px 25px;
}
}

@media (max-width: 500px) {
    .main-container {
    padding: 25px 0px 0px 25px;
    max-width: 308px;
    margin: 0 auto;
}
}

</style>