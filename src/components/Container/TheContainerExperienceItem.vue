<script>
export default {
    name: 'TheContainerEducationItem',
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
        location: {
            type: String,
            requierd: true,

        },
        description: {
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
    <li>
        <div class="experince-item">
            <div class="experience-info">
                <div class="experience-info-top">
                    <div class="experience-date">{{ date }}</div>
                    <img src="/svg/location.svg" />
                    <div class="experience-location">{{ location }}</div>
                </div>
                <div class="experience-info-bottom">
                   <img :src="icon" class="experience-icon" />
                   <div class="experience-info-bottom-text">
                    <div class="experience-title">{{ title }}</div>
                    <div class="experience-company"> {{ company }}</div>
                   </div>
                </div>
            </div>
        
        <div class="experience-description">{{ description }}</div>

        </div>
    </li>
    

</template>

<style scoped>
.experince-item {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
}
.experience-info {
    width: 100%;
    max-width: 242px;
    margin-left: 16px;
}
.experience-info-top {
    display: flex;
    gap: 5px;
    align-items: center;
    margin-bottom: 10px;
}
.experience-info-bottom {
    display: flex;
    margin-bottom: 10px;
    gap: 16px

}
.experience-info-bottom-text {
    display: flex;
    flex-direction: column;
    text-align: start;
    gap: 5px;
}
.experience-location {
    font-family: var(--font-family);
    font-weight: 400;
    font-size: 10px;
    letter-spacing: 0.01em;
    color: #79819a;
}

.experience-date {
    font-family: var(--font-family);
    font-weight: 400;
    font-size: 10px;
    letter-spacing: 0.01em;
    color: #47516b;
}
.experience-title {
    font-family: var(--font-family);
    font-weight: 400;
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
}
.experience-company {
    font-family: var(--font-family);
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #2e2e48;
}
.experience-description {
    font-family: var(--font-family);
    font-weight: 400;
    font-size: 12px;
    letter-spacing: 0.01em;
    color: #79819a;
    width: 100%;
    max-width: 407px;
    text-align: start;
}
.experience-icon {
    width: 49px;
    height: 49px;
    border-radius: 50%;
}


@media (max-width: 1025px) {
   .experince-item {
    flex-direction: column;
   }
}

@media (max-width: 1025px) {
    .experience-description {
    max-width: 300px;
   }



}

</style>