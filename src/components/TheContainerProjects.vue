<script>
import TheContainerProjectsItem from './TheContainerProjectsItem.vue';

export default {
    name: 'TheContainerExperience',
    components: { TheContainerProjectsItem },
    data() {
        return {
        projects: [
        {
            id: 1,
            icon: "/svg/miina.svg",
            title:"Miina Group E-commerce",
            subtitle: "E-commerce platform",
            link: "https://www.miinagroup.com.au/"
        },
        {
            id: 2,
            icon: "/svg/problematic.svg",
            title:"Problematic Media landing page",
            subtitle: "Landing page with GSAP usage",
            link: "https://www.problematic.com.au/"
        }
    ]
        }
    }
    
};
</script>

<template>
        <div class="component-title"><div class="spot-tick"></div>Latest Projects</div>
        <div class="project-list-wrapper">
            <div class="divider"></div>
            <div class="project-list">
            <TheContainerProjectsItem
            v-for="project in projects"
            :key="project.id"
            :title="project.title"
            :subtitle="project.subtitle"
            :icon="project.icon"
            :link="project.link"
        />
        </div>
        </div>
</template>

<style scoped>
.project-list-wrapper {
    display: flex;
    margin-left: 2px;
}
.project-list {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 32px;
    width: 100%;
}

@media (max-width: 1025px) {
   .project-list {
    flex-direction: column;
    gap: 16px;
    align-items: flex-start;
   }
}

@media (max-width: 500px) {
    .project-list {
        padding: 32px 0px 32px 10px
    }
}



</style>