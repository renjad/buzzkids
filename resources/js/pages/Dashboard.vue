<script setup lang="ts">
import { Head } from '@inertiajs/vue3';
import AppLayout from '@/layouts/AppLayout.vue';
import { dashboard } from '@/routes';
import { type BreadcrumbItem } from '@/types';
import PlaceholderPattern from '../components/PlaceholderPattern.vue';

import {
    Select,
    SelectContent,
    SelectGroup,
    SelectItem,
    SelectLabel,
    SelectTrigger,
    SelectValue,
} from '@/components/ui/select';

const breadcrumbs: BreadcrumbItem[] = [
    {
        title: 'Dashboard',
        href: dashboard().url,
    },
];
</script>

<template>
    <Head title="Dashboard" />

    <AppLayout :breadcrumbs="breadcrumbs">
        <!-- <Select>
            <SelectTrigger class="w-45">
                <SelectValue placeholder="Select a fruit" />
            </SelectTrigger>
            <SelectContent>
                <SelectGroup>
                    <SelectItem value="apple"> Apple </SelectItem>
                    <SelectItem value="banana"> Banana </SelectItem>
                    <SelectItem value="blueberry"> Blueberry </SelectItem>
                    <SelectItem value="grapes"> Grapes </SelectItem>
                    <SelectItem value="pineapple"> Pineapple </SelectItem>
                    <SelectItem value="apple"> Apple </SelectItem>
                    <SelectItem value="banana"> Banana </SelectItem>
                    <SelectItem value="blueberry"> Blueberry </SelectItem>
                    <SelectItem value="grapes"> Grapes </SelectItem>
                    <SelectItem value="pineapple"> Pineapple </SelectItem>
                    <SelectItem value="apple"> Apple </SelectItem>
                    <SelectItem value="banana"> Banana </SelectItem>
                    <SelectItem value="blueberry"> Blueberry </SelectItem>
                    <SelectItem value="grapes"> Grapes </SelectItem>
                    <SelectItem value="pineapple"> Pineapple </SelectItem>
                    <SelectItem value="apple"> Apple </SelectItem>
                    <SelectItem value="banana"> Banana </SelectItem>
                    <SelectItem value="blueberry"> Blueberry </SelectItem>
                    <SelectItem value="grapes"> Grapes </SelectItem>
                    <SelectItem value="pineapple"> Pineapple </SelectItem>
                    <SelectItem value="apple"> Apple </SelectItem>
                    <SelectItem value="banana"> Banana </SelectItem>
                    <SelectItem value="blueberry"> Blueberry </SelectItem>
                    <SelectItem value="grapes"> Grapes </SelectItem>
                    <SelectItem value="pineapple"> Pineapple </SelectItem>
                    <SelectItem value="apple"> Apple </SelectItem>
                    <SelectItem value="banana"> Banana </SelectItem>
                    <SelectItem value="blueberry"> Blueberry </SelectItem>
                    <SelectItem value="grapes"> Grapes </SelectItem>
                    <SelectItem value="pineapple"> Pineapple </SelectItem>
                </SelectGroup>
            </SelectContent>
        </Select> -->

        <div
            class="flex h-full flex-1 flex-col gap-4 overflow-x-auto rounded-xl p-4"
        >
            <div class="grid auto-rows-min gap-4 md:grid-cols-3">
                <div
                    class="relative aspect-video overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border"
                >
                    <PlaceholderPattern />
                </div>
                <div
                    class="relative aspect-video overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border"
                >
                    <PlaceholderPattern />
                </div>
                <div
                    class="relative aspect-video overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border"
                >
                    <PlaceholderPattern />
                </div>
            </div>
            <div
                class="relative min-h-[100vh] flex-1 rounded-xl border border-sidebar-border/70 md:min-h-min dark:border-sidebar-border"
            >
                <PlaceholderPattern />
            </div>
        </div>
    </AppLayout>
</template>
