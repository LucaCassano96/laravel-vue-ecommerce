
<template>
    <!-- Header -->

    <header class="h-20 shadow bg-white items-center flex justify-between p-3">
        <button @click="emit('toggle-sidebar')" class="flex items-center justify-center rounded w-10 h-10 'text-gray-700 hover:bg-black/10 transition-colors">
            <Bars3Icon class="w-9"></Bars3Icon>
        </button>

            <Menu as="div" class="relative inline-block text-left">
                    <MenuButton class="flex items-center">
                        <img class="rounded-full w-12 mr-2" src="https://randomuser.me/api/portraits/men/81.jpg" alt="">
                        Jhon Smith
                        <ChevronDownIcon class="h-5 w-5 text-violet-200 hover:text-violet-100" aria-hidden="true" />
                    </MenuButton>


                <transition enter-active-class="transition duration-100 ease-out"
                    enter-from-class="transform scale-95 opacity-0" enter-to-class="transform scale-100 opacity-100"
                    leave-active-class="transition duration-75 ease-in" leave-from-class="transform scale-100 opacity-100"
                    leave-to-class="transform scale-95 opacity-0">
                    <MenuItems
                        class="absolute right-0 mt-2 w-36 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
                        <div class="px-1 py-1">
                            <MenuItem v-slot="{ active }">
                            <button :class="[
                                active ? 'bg-indigo-600 text-white' : 'text-gray-900',
                                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                            ]">
                                <UserIcon :active="active" :class="[
                                    active ? 'bg-indigo-600 text-white' : 'text-gray-900',
                                    'mr-2 h-5 w-5',
                                ]" aria-hidden="true" />
                                Profile
                            </button>
                            </MenuItem>
                            <MenuItem v-slot="{ active }">
                            <button :class="[
                                active ? 'bg-indigo-600 text-white' : 'text-gray-900',
                                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
                            ]">
                                <ArrowLeftIcon :active="active" :class="[
                                    active ? 'bg-indigo-600 text-white' : 'text-gray-900',
                                    'mr-2 h-5 w-5',
                                ]" aria-hidden="true" />
                                Logout
                            </button>
                            </MenuItem>
                        </div>
                    </MenuItems>
                </transition>
            </Menu>

    </header>
</template>

<script setup>

import { Bars3Icon, UserIcon, ArrowLeftIcon } from '@heroicons/vue/24/outline'
import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'
import { ChevronDownIcon } from '@heroicons/vue/20/solid'

const emit = defineEmits(
    ['toggle-sidebar']
)

</script>


