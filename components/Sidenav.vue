<template>
    <nav class="bg-[#F5F5F5] shadow-[inset_-1px_0px_0px_#D1D4DB]">
        <ul class="">
            <template v-for="(nav , index) in navigation" :key="index">
                <NuxtLink :to="{name: nav?.name}">
                    <li :class="$route?.name == nav.name ? 'bg-[#E0E0E0] shadow-[inset_0px_-1px_0px_#D1D4DB]' : ''" class="hover:bg-[#e0e0e050] text-[#212143] font-medium px-6 py-4 transition ease-linear flex items-center space-x-2 cursor-pointer">
                            <Icon :name="nav?.icon" />  <span>{{ nav?.title }}</span>
                    </li>
                </NuxtLink>
            </template>
        </ul>
    </nav>
</template>

<script>
export default {
    data(){
        return {
            navigation: [
                {
                    name: "index",
                    title: "Dashboard",
                    icon: "akar-icons:home"
                },
                {
                    name: "job",
                    title: "Job Desk",
                    icon: "bx:briefcase-alt-2"
                },
                {
                    name: "employee",
                    title: "Employee",
                    icon: "ic:outline-person-outline",
                    sub: [
                        {
                            name: "employee",
                            title: "All Employees"
                        },
                        {
                            name: "appointment",
                            title: "Appointment"
                        },
                    ]
                },
                {
                    name: "leave",
                    title: "Leave",
                    icon: "ph:arrow-line-left",
                    sub: [
                        {
                            name: "employee",
                            title: "Status"
                        },
                        {
                            name: "appointment",
                            title: "Request"
                        },
                        {
                            name: "employee",
                            title: "Calendar"
                        },
                        {
                            name: "appointment",
                            title: "Summary"
                        },
                    ]
                },
                {
                    name: "attendance",
                    title: "Attendance",
                    icon: "mdi:clock-time-three-outline",
                    sub: [
                        {
                            name: "employee",
                            title: "Daily Log"
                        },
                        {
                            name: "appointment",
                            title: "Request"
                        },
                        {
                            name: "employee",
                            title: "Details"
                        },
                        {
                            name: "appointment",
                            title: "Summary"
                        },
                    ]
                },
                {
                    name: "admin",
                    title: "Administration",
                    icon: "ph:folder",
                    sub: [
                        {
                            name: "employee",
                            title: "Role"
                        },
                        {
                            name: "appointment",
                            title: "Shift"
                        },
                        {
                            name: "employee",
                            title: "Department"
                        },
                        {
                            name: "appointment",
                            title: "Holiday"
                        },
                        {
                            name: "appointment",
                            title: "Announcement"
                        },
                    ]
                },
                {
                    name: "setting",
                    title: "Settings",
                    icon: "ic:outline-settings",
                    sub: [
                        {
                            name: "employee",
                            title: "General"
                        },
                        {
                            name: "appointment",
                            title: "Leave"
                        },
                        {
                            name: "employee",
                            title: "Attendance"
                        },
                        {
                            name: "appointment",
                            title: "Payroll"
                        },
                        {
                            name: "appointment",
                            title: "Import"
                        },
                    ]
                },
            ]
        }
    }
}
</script>