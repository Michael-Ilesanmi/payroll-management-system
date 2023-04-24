<template>
    <div class="layout">
        <Navbar class="navbar" />
        <Sidenav class="sidenav"/>
        <div class="main_section p-8">
            <slot />
        </div>
    </div>
</template>

<style scoped>
.layout {
    grid-template-rows: 50px 1fr;
    grid-template-columns: 250px 1fr;
    grid-template-areas: 
        "nav nav"
        "side main"; 
    @apply bg-[#EAEAEA] h-screen min-h-screen grid fixed top-0 left-0 right-0 bottom-0;
}
.navbar {
    grid-area: nav;
}

.sidebar {
    grid-area: side;
    overflow-y: scroll;
}
.main_section {
    grid-area: main;
    @apply overflow-y-scroll pb-48;
}
</style>