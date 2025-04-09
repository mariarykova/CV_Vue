
<script>
import TheContainerSkillsItem from './TheContainerSkillsItem.vue';

export default {
    name: 'TheContainerExperience',
    components: { TheContainerSkillsItem },
    data() {
        return {
        skills: [
        {
            id: 1,
            icon: "/svg/figma.svg",
            title:"Figma",
            subtitle: "Web UI Design, Prototyping"
        },
        {
            id: 2,
            icon: "/svg/html.svg",
            title:"HTML 5",
            subtitle: "Structural Design"
        },
        {
            id: 3,
            icon: "/svg/css.svg",
            title:"CSS",
            subtitle: "Style Design"
        },
        {
            id: 4,
            icon: "/svg/react.svg",
            title:"React JS",
            subtitle: "Interface Design, Web Development"
        },
        {
            id: 5,
            icon: "/svg/vue.svg",
            title:"Vue JS",
            subtitle: "Interface Design, Web Development"
        },
        {
            id: 6,
            icon: "/svg/typescript.svg",
            title:"TypeScript",
            subtitle: "Web Development"
        },
    ]
        }
    }
    
};
</script>

<template>
        <div class="component-title"><div class="spot-tick"></div>Tools/Skills</div>
        <div class="skills-list-wrapper">
            <div class="divider"></div>
            <div class="skills-list">
            <TheContainerSkillsItem
            v-for="skill in skills"
            :key="skill.id"
            :title="skill.title"
            :subtitle="skill.subtitle"
            :icon="skill.icon"
        />
            </div>
        </div>
</template>

<style scoped>

.skills-list-wrapper {
    display: flex;
    margin-left: 2px;
    
    
}
.skills-list {
    display: flex;
    flex-wrap: wrap;
    padding: 32px;
    width: 100%;
    max-width: 698px;
    gap: 50px;
    justify-content: center;
}
</style>
