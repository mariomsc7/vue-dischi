<template>
    <header>
        <div class="logo">
            <img src="@/assets/logo.png" alt="">
        </div>
    </header>
</template>

<script>

export default {
    name: 'Header',
}
</script>

<style scoped lang="scss">
    @import '@/scss/general.scss';

    header {
        height: 70px;
        background: $header-bg-color;
    }

    .logo {
        height: 100%;
        display: flex;
        align-items: center;
        padding: 10px;
    }

    .logo {
        img {
            width: 64px;
            padding: 5px;
        }
    }

</style>