<template>
    <div id="navbar">
        <div class="menu-link">
            <a href="#">Laura <br> Caillaux</a>
        </div>
        <div class="menu-link">
            Menu
        </div>
        <div class="menu-link">
            About
        </div>
    </div>
</template>

<style lang="scss" scoped>
#navbar {
    border: 1px solid red;
    height: 130px;
    font-family: $ff-sans;
    font-size: 28px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    & .menu-link {
        width: 120px;
        text-align: center;
    }
}

</style>
