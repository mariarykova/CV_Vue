<script>
import myPhoto from '../assets/images/photo.jpeg';
import TheAsideContactsList from './TheAsideContactsList.vue'
import TheAsideHobbiesList from './TheAsideHobbiesList.vue';
import TheAsideLanguagesList from './TheAsideLanguagesList.vue';
import TheAsideSocialList from './TheAsideSocialList.vue';


export default {
    name: "MyPhoto",
    components: {
        TheAsideContactsList,
        TheAsideSocialList,
        TheAsideLanguagesList,
        TheAsideHobbiesList
    },
    data() {
        return {
            photoUrl: myPhoto,
            altText: "Maria Rykova",
            contacts : [
                {id: 1, icon: "/svg/email.svg", title: "Email", text: "mari.reekova@gmail.com"},
                {id: 2, icon: "/svg/phone.svg", title: "Phone", text: "+61 448 381 158"},
                {id: 3, icon: "/svg/address.svg", title: "Addres", text: "Perth, Australia"},
            ],
            socials: [
                {id: 1, icon: "/svg/linkedin.svg", title: "LinkedIn", text: "@maria-rykova"},
                {id: 2, icon: "/svg/github.svg", title: "GitHub", text: "@mariarykova"},
            ],
            languages: [
                {id: 1, icon: "/svg/russian.svg", title: "Russian", text: "Native"},
                {id: 2, icon: "/svg/english.svg", title: "English", text: "Professional working"},
                {id: 3, icon: "/svg/french.svg", title: "French", text: "Speaking"},
                {id: 4, icon: "/svg/italian.svg", title: "Italian", text: "Basic"},
            ],
            hobbies: [
                {id: 1, icon: "/svg/dog.svg", title: "", text: "Animals"},
                {id: 2, icon: "/svg/book.svg", title: "", text: "Reading"},
                {id: 3, icon: "/svg/sport.svg", title: "", text: "Sport"},
            ]
        }
    }
}
</script>

<template>
    <div class="aside">
        <div class="aside-photo">
            <img :src="photoUrl" :alt="altText" class="photo" />
        </div>
        <div class="aside-name">Maria Rykova</div>
        <p class="aside-quote">Results-oriented Frontend Developer with 4 years of professional experience, specialising in developing user-friendly web applications. I am familiar with Agile methodology. Through my career, I have participated in projects in diverse industries: Banking, Renting Services, Blockchain, Media Production, Sustainability, E-commerce.</p>
        <div class="aside-divider"></div>
        <TheAsideContactsList :contacts="contacts"/>
        <div class="aside-divider"></div>
        <h4 class="aside-subtitle">Socials</h4>
        <TheAsideSocialList :socials="socials"/>
        <div class="aside-divider"></div>
        <h4 class="aside-subtitle">Languages</h4>
        <TheAsideLanguagesList :languages="languages"/>
        <div class="aside-divider"></div>
        <h4 class="aside-subtitle">Hobbies & Interests</h4>
        <TheAsideHobbiesList :hobbies="hobbies"/>
    </div>
</template>
  
  <style scoped>
 .aside {
    background-color: #f7f9fc;
    width: 100%;
    max-width: 258px;
    padding: 48px;
    text-align: left;
 }
 .photo {
    border-radius: 50%;
    width: 100%;
    height: 100%;
    max-width: 96px;
    max-height: 96px;
    object-fit: cover;
 }
 .aside-name {
    font-family: var(--second-family);
    font-weight: 500;
    font-size: 32px;
    line-height: 125%;
    letter-spacing: -0.02em;
    color: #2e2e48;
    padding-top: 16px;
 }
 .aside-quote {
    width: 100%;
    max-width: 280px;
    font-family: var(--second-family);
    font-weight: 500;
    font-size: 18px;
    line-height: 133%;
    letter-spacing: 0.02em;
    color: #47516b;
 }
 .aside-divider {
    border: 1px solid #e2e6ee;
    width: 266px;
 }
 .aside-subtitle {
    font-family: var(--font-family);
        font-weight: 400;
        font-size: 12px;
        line-height: 133%;
        letter-spacing: 0.01em;
        color: #e5e5e5;
 }
  </style>