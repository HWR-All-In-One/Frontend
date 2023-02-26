<template>
    <div>
        <h1 class="page-title">Stundenplan</h1>
        <ScheduleList />
        <Schedule />
    </div>
</template>

<script>
import Schedule from '~/components/Schedule.vue';
import ScheduleList from '~/components/ScheduleList.vue';

export default {
    name: "schedule",
    components: {
        Schedule,
        ScheduleList,
    }
}
</script>

<style lang="scss">
/* Dark Theme Styling */


/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.page-title {
    margin: 1rem 0;
}
</style>
