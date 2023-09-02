<template>
    <div class="navbar-wrapper">
        <nav class="mobile-navbar-wrapper">
            <div class="mobile-navbar">
                <img src="../assets/logo.svg" alt="">
                <button v-show="!isActive" @click="isActive = !isActive"><img src="../assets/icon-hamburger.svg" alt=""></button>
                <button v-show="isActive" @click="isActive = !isActive"><img src="../assets/icon-close.svg" alt="" ></button>
            </div>
            <div class="mobile-navbar-active" v-show="isActive">
                <ul class="mobile-navbar-links">
                    <li v-for="(link, index) in links" :key="index" class="mobile-navbar-link"><a href="#">{{ link }}</a></li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const links = ['Home', 'About', 'Contact', 'Blog', 'Careers']
const isActive = ref(false)
</script>

<style scoped>
.navbar-wrapper .mobile-navbar-wrapper {
    position: relative;
}
.navbar-wrapper .mobile-navbar-wrapper .mobile-navbar {
    display: flex;
    padding: 1.375rem 1.5rem;
    align-items: center;
    justify-content: space-between;
}
.navbar-wrapper .mobile-navbar-wrapper .mobile-navbar button {
    background: none;
    border: none;
}
.navbar-wrapper .mobile-navbar-wrapper .mobile-navbar-active {
    position: absolute;
    z-index: 10;
    left: 0;
    right: 0;
    margin: 0 auto;
    display: flex;
    justify-content: center;
}
.navbar-wrapper .mobile-navbar-wrapper .mobile-navbar-active .mobile-navbar-links {
    padding: 2.25rem 8.25rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    list-style-type: none;
    background-color: var(--White);
    border-radius: 0.25rem;
}
.navbar-wrapper .mobile-navbar-wrapper .mobile-navbar-active .mobile-navbar-links li a {
    text-decoration: none;
    color: var(--Dark-Blue);
}
</style>