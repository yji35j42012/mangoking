<template>
    <header class="header">
        <h1 class="logo">
            <router-link to="/">
                <img src="~/assets/images/logo.svg" alt="" />
            </router-link>
        </h1>
        <ul class="nav">
            <li class="nav__btn">
                <router-link to="/portfolio">Portfolio</router-link>
            </li>
            <li class="nav__btn">
                <router-link to="/product">Product</router-link>
            </li>
            <li class="nav__btn">
                <router-link to="/download">Download</router-link>
            </li>
            <li class="nav__btn">
                <router-link to="/about">About Us</router-link>
            </li>
        </ul>
    </header>
</template>