<template>

    <b-navbar  class="nav-style">
        <template #brand>
            <b-navbar-item tag="router-link" :to="{ path: '/' }">
                <img
                        src="@/assets/logo.png"
                        alt="Lightweight UI components for Vue.js based on Bulma"
                >
            </b-navbar-item>
        </template>
        <template #start>
            <b-navbar-item href="#">
                Home
            </b-navbar-item>
            <b-navbar-item href="#">
                Documentation
            </b-navbar-item>
            <b-navbar-dropdown label="Info">
                <b-navbar-item href="#">
                    About
                </b-navbar-item>
                <b-navbar-item href="#">
                    Contact
                </b-navbar-item>
            </b-navbar-dropdown>
        </template>

        <template #end>
            <b-navbar-item tag="div">
                <div class="buttons">
                    <router-link to="/register" class="button btn--green signup">
                        <strong>Sign up</strong>
                    </router-link>
                    <router-link to="/login" class="button login is-light">
                        Log in
                    </router-link>
                </div>
            </b-navbar-item>
        </template>
    </b-navbar>

</template>
