
<script>
import TheContainerExperienceItem from './TheContainerExperienceItem.vue';

export default {
    name: 'TheContainerExperience',
    components: { TheContainerExperienceItem },
    data() {
        return {
        works: [
        {
            id: 1,
            title: 'Frontend Developer',
            company: 'Problematic Media',
            date: 'Jun 2024 - Feb 2025',
            location: 'Remote',
            description: 'I was responsible for designing and developing web pages using Figma, including creating key pages and translating those designs into responsive, interactive web applications using ReactJS, GASP, ThreeJS, and NodeJS. I also developed backend functionality, such as implementing search features and user registration systems, and managed data storage using MongoDB to ensure efficient and scalable backend solutions.',
            icon: "/svg/media.svg",
        },
        {
            id: 2,
            title: 'Frontend Developer',
            company: 'Fluidity.Money',
            date: 'Nov 2023 - Feb 2024',
            location: 'Remote',
            description: 'I developed a Leaderboard ranking page using NextJS and ReactJS, ensuring a dynamic and responsive user experience. I integrated blockchain wallets using the Wagmi library and created SQL queries to interact with databases, as well as GraphQL queries to retrieve data from The Graph. Additionally, I implemented unit and end-to-end tests with Cypress, ensuring robust and reliable functionality across the application.',
            icon: "/svg/fluidity.svg",
        },
        {
            id: 3,
            title: 'Frontend Developer',
            company: 'SberBank',
            date: 'Dec 2021 - Jan 2023',
            location: 'Remote',
            description: 'I played a pivotal role in teams of 7 and 20 members, contributing to the development of fraud prevention and multi-source data search system projects. I led the front-end development and component redesign for both projects, overseeing the entire process from inception to final product. Working closely with bank IT security teams, I ensured software infrastructure permissions were in place and maintained a secure development environment. I also introduced enhanced user request logic and resolved several bugs, improving system functionality and reliability. Throughout these projects, I leveraged a comprehensive tech stack including React JS, TypeScript, Redux-Toolkit, React Test Library, Jest, and React Final Form. Additionally, I facilitated a cohesive agile workflow across frontend, backend, DevOps, and testing teams, ensuring smooth and efficient project delivery.',
            icon: "/svg/sber.svg",
        },
        {
            id: 4,
            title: 'Frontend Developer',
            company: 'Everypixel Group',
            date: 'Oct 2020 - Dec 2021',
            location: 'Remote',
            description: "I transitioned jQuery components to React JS on the EveryPixel Free Exclusive platform, significantly enhancing performance and user experience. I also engineered new features, including file structures for upcoming multilingual support and synchronized desktop/mobile versions on photo pages. By optimizing the website’s performance using Lighthouse, I achieved exceptional performance benchmarks for mobile devices. Additionally, I collaborated closely with a senior frontend colleague to design and develop the Color Trends page.",   
            icon: "/svg/everypixel.svg",
        },
    ]
        }
    }
    
};
</script>

<template>
        <div class="component-title"><div class="spot-tick"></div>Experience</div>
        <div class="experience-list">
            <div class="divider"></div>
            <ul>
            <TheContainerExperienceItem
            v-for="work in works"
            :key="work.id"
            :title="work.title"
            :company="work.company"
            :date="work.date"
            :location="work.location"
            :description="work.description"
            :icon="work.icon"
        />
        </ul>
        </div>
</template>

<style scoped>
.experience-list {
    display: flex;
    margin-left: 2px;
}
</style>