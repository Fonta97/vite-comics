<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                {
                    text: 'CHARACTERS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COMICS',
                    url: '#',
                    current: true,
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'GAMES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'FANS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'NEWS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'SHOP',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <img src="../../public/img/dc-logo.png" alt="">
            <ul>
                <li v-for="link in links">
                    <a :class="link.current ? 'active' : ''" :href="link.url">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.container {
    display: flex;
    justify-content: space-between;

    img {
        padding: 1rem;
    }

    ul {
        list-style: none;
        @include center();

        li a {
            display: inline-block;
            padding: 3.5rem 0.5rem;
            text-decoration: none;
            font-weight: 600;
            color: $grey;

            &.active,
            &:hover {
                border-bottom: 5px solid $primary;
                color: $primary;
            }
        }
    }
}
</style>