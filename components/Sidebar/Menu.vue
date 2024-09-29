<script setup>
const items = ref([
    {
        title:"Projects",
        path: "/projects",
        icon: "ant-design:project-outlined"
    },
    {
        title: "Tasks",
        path: "/tasks",
        icon: "la:tasks"
    },
    {
        title:"Analytics",
        path: "/analytics",
        icon: "carbon:analytics"
    },
    {
        title:"Calendar",
        path: "/calendar",
        icon: "ion:calendar-outline"
    },
    {
        title:"Board",
        path: "/board",
        icon: "tabler:layout-kanban"
    },
    {
        title:"Account",
        path: "/account",
        icon: "codicon:account"
    },
    {
        title:"Teams",
        path: "/teams",
        icon: "ant-design:team-outlined"
    },
    {
        title:"Settings",
        path: "/settings",
        icon: "material-symbols:settings-outline"
    },
    {
        title:"Market",
        path: "/market",
        icon: "icon-park-outline:weixin-market"
    }
])
</script>

<template>
    <div>
        <header class="flex items-center gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
            <Logo />
            <p class="font-bold">Timeman</p>
        </header>
        <div class="px-4 grow">
            <div class="grid gap-2">
                <NuxtLink :href="item.path" v-for="(item,index) in items" :key="index" class="flex items-center gap-2 px-2 py-1 transition rounded cursor-pointer hover:bg-neutral-100">
                    <Icon size="20" :name="item.icon" color="black" />
                    <span>{{ item.title }}</span>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>
<style scoped>
    
</style>