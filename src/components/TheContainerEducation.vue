
<script>
import TheContainerEducationItem from './TheContainerEducationItem.vue';

export default {
    name: 'TheContainerEducation',
    components: { TheContainerEducationItem },
    data() {
        return {
        educations: [
        {
            id: 1,
            icon: "/svg/vavt.svg",
            name: "VAVT",
            degree: 'Specialist in International Economics',
            date: '2007 - 2012',
        }
    ]
        }
    }
    
};
</script>

<template>
        <div class="component-title"><div class="spot-tick"></div>Education</div>
        <div class="education-list">
            <div class="divider"></div>
            <TheContainerEducationItem
            v-for="education in educations"
            :key="education.id"
            :name="education.name"
            :degree="education.degree"
            :date="education.date"
            :icon="education.icon"
        />
        </div>
</template>

<style scoped>
.education-list {
    display: flex;
    margin-left: 2px;
}
</style>