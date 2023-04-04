<template>
    <nav 
        class="bg-[#F5F5F5] shadow-[inset_-1px_0px_0px_#D1D4DB] overflow-y-scroll pb-24"
    >
        <ul>
            <template 
                v-for="(nav , index) in navigation" 
                :key="index"
            >
                <NuxtLink 
                    :to="{name: nav?.sub ? false : nav?.name}" 
                    @click="nav.open = !nav.open"
                >
                    <li 
                        :class="($route?.name == nav?.name) || $route?.name?.includes(`${nav?.name}-`) ? 'bg-[#E0E0E0] shadow-[inset_0px_-1px_0px_#D1D4DB]' : 'hover:bg-[#e0e0e050]'" 
                        class="text-[#212143] font-medium px-6 py-4 transition ease-linear flex items-center space-x-2 cursor-pointer"
                    >
                            <Icon :name="nav?.icon" size="1.3em" />
                            <span>{{ nav?.title }}</span>
                            <i v-if="nav?.sub" :class="nav?.open ? 'fa-angle-up' : 'fa-angle-down'" class="fa-solid !ml-auto"></i>
                    </li>
                </NuxtLink>
                <div 
                    v-show="nav?.sub && nav?.open == true">
                    <div 
                        v-for="(item , index) in nav.sub" 
                        :key="index"
                    >
                        <NuxtLink 
                            :to="{name: item?.name ?? false}"
                        >
                            <li 
                                :class="$route?.name == item.name ? 'bg-[#D3D3D9]' : 'hover:bg-[#e0e0e050]'" 
                                class="text-[#212143] font-medium py-2 px-4 m-2 rounded-md text-sm transition ease-linear cursor-pointer"
                            >
                                {{item?.title}}
                            </li>
                        </NuxtLink>
                    </div>
                </div>
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
                    open: false,
                    icon: "akar-icons:home"
                },
                {
                    name: "job",
                    title: "Job Desk",
                    open: false,
                    icon: "bx:briefcase-alt-2"
                },
                {
                    name: "employee",
                    title: "Employee",
                    icon: "ic:outline-person-outline",
                    open: false,
                    sub: [
                        {
                            name: "employee",
                            title: "All Employees"
                        },
                        {
                            name: "employee-appointment",
                            title: "Appointment"
                        },
                    ]
                },
                {
                    name: "leave",
                    title: "Leave",
                    icon: "ph:arrow-line-left",
                    open: false,
                    sub: [
                        {
                            name: "leave",
                            title: "Status"
                        },
                        {
                            name: "leave-request",
                            title: "Request"
                        },
                        {
                            name: "leave-calendar",
                            title: "Calendar"
                        },
                        {
                            name: "leave-summary",
                            title: "Summary"
                        },
                    ]
                },
                {
                    name: "attendance",
                    title: "Attendance",
                    icon: "mdi:clock-time-three-outline",
                    open: false,
                    sub: [
                        {
                            name: "attendance",
                            title: "Daily Log"
                        },
                        {
                            name: "attendance-request",
                            title: "Request"
                        },
                        {
                            name: "attendance-details",
                            title: "Details"
                        },
                        {
                            name: "attendance-summary",
                            title: "Summary"
                        },
                    ]
                },
                {
                    name: "admin",
                    title: "Administration",
                    icon: "ph:folder",
                    open: false,
                    sub: [
                        {
                            name: "admin",
                            title: "Role"
                        },
                        {
                            name: "admin-shift",
                            title: "Shift"
                        },
                        {
                            name: "admin-department",
                            title: "Department"
                        },
                        {
                            name: "admin-holiday",
                            title: "Holiday"
                        },
                        {
                            name: "admin-announcement",
                            title: "Announcement"
                        },
                    ]
                },
                {
                    name: "setting",
                    title: "Settings",
                    icon: "ic:outline-settings",
                    open: false,
                    sub: [
                        {
                            name: "setting",
                            title: "General"
                        },
                        {
                            name: "setting-leave",
                            title: "Leave"
                        },
                        {
                            name: "setting-attendance",
                            title: "Attendance"
                        },
                        {
                            name: "setting-payroll",
                            title: "Payroll"
                        },
                        {
                            name: "setting-import",
                            title: "Import"
                        },
                    ]
                },
            ]
        }
    }
}
</script>