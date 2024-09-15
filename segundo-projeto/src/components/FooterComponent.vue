<template>
    <footer>

        <a class="socialLink" v-for="(socialLink, index) in socialLinks" :key="index" :href="socialLink.link" target="_blank">
            <img :alt="socialLink.label" :title="socialLink.label" :src="socialLink.icon"/>
        </a>

        <p>&copy; 2024 Your Company. All rights reserved.</p>
    </footer>
</template>

<script>
import api from '@/services/api';

export default {
    name: 'FooterComponent',
    data(){
        return {
            socialLinks: []
        }
    },
    mounted(){
        api.get('/social-links.json').then(response => {
            this.socialLinks = response.data;
        });
    }
}
</script>

<style scoped>
    footer{
        background-color: var(--color-background-nav);
        color: var(--color-text-light);
        width: 100%;
        height: 60px;
        display: flex;
        text-align: center;
        justify-content: center;
        align-items: center;
    }

    .socialLink img{
        width: 20px;
    }

    .socialLink{
        border: 2px solid var(--color-text-light);
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        width: 40px;
        height: 40px;
        margin: 0 10px;
    }

</style>