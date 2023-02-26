<template>
    <div>
        <v-row class="schedule fill-height">
            <v-col>
                <v-sheet height="64">
                    <v-toolbar flat>
                        <v-btn outlined class="mr-4" color="grey darken-2" @click="setToday">
                            Heute
                        </v-btn>
                        <v-btn fab text small color="grey darken-2" @click="prev">
                            <v-icon small>
                                mdi-chevron-left
                            </v-icon>
                        </v-btn>
                        <v-btn fab text small color="grey darken-2" @click="next">
                            <v-icon small>
                                mdi-chevron-right
                            </v-icon>
                        </v-btn>
                        <v-toolbar-title v-if="$refs.calendar">
                            {{ $refs.calendar.title }}
                        </v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-menu bottom right>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn outlined color="grey darken-2" v-bind="attrs" v-on="on">
                                    <span>{{ typeToLabel[type] }}</span>
                                    <v-icon right>
                                        mdi-menu-down
                                    </v-icon>
                                </v-btn>
                            </template>
                            <v-list>
                                <v-list-item @click="type = 'day'">
                                    <v-list-item-title>
                                        Tag
                                    </v-list-item-title>
                                </v-list-item>
                                <v-list-item @click="type = 'week'">
                                    <v-list-item-title>
                                        Woche
                                    </v-list-item-title>
                                </v-list-item>
                                <v-list-item @click="type = 'month'">
                                    <v-list-item-title>
                                        Monat
                                    </v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </v-toolbar>
                </v-sheet>
                <v-sheet height="600">
                    <v-calendar locale="de" :interval-format="intervalFormat" :first-interval="7"
                        :interval-count="15" interval-height="34.58" ref="calendar" v-model="focus" color="primary" :events="events" :event-color="getEventColor"
                        :type="type" @click:event="showEvent" @click:more="viewDay" @click:date="viewDay"
                        @change="updateRange"></v-calendar>
                    <v-menu color="grey lighten-4" v-model="selectedOpen" :close-on-content-click="false" :activator="selectedElement" offset-x>
                        <v-card min-width="350px" flat>
                            <v-toolbar :color="selectedEvent.color" dark>
                                <v-toolbar-title v-html="selectedEvent.name"></v-toolbar-title>
                            </v-toolbar>
                        </v-card>
                    </v-menu>
                </v-sheet>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    name: "schedule",
    components: {
        ListItem: () => import("./ListItem.vue")
    },
    data: () => ({
        colors: ['#1576d0'],
        events: [],
        focus: '',
        intervalFormat: '',
        names: [
            'Datenanalyse - Raum: Online - Prof. Dr. Höhne',
            'Labor SWE II - Gruppe 2 - Raum: 6B.052 - B.Sc. Stricker',
            'Labor SWE II - Gruppe 1 - Raum: 6B.052 - B.Sc. Stricker',
            'Optimierte Verfahren - Raum: 6B.173 - Prof. Dr. Winter',
            'C++ - Raum: 6B.052 - Puschmann',
            'Skriptsprachen - Raum: 6B.052 - B.Sc. Löchner',
            'SWE II - Raum: 6B.450 - B.Sc. Stricker',
            'Webprogrammierung - Raum: Online - B.Sc. Brunkow',
        ],
        selectedElement: null,
        selectedEvent: {},
        selectedOpen: false,
        type: 'week',
        typeToLabel: {
            month: 'Monat',
            week: 'Woche',
            day: 'Tag',
        },
    }),
    mounted() {
        this.$refs.calendar.checkChange()
    },
    methods: {
        getEventColor(event) {
            return event.color
        },
        intervalFormatter(locale, getOptions) {
            return locale.time;
        },
        next() {
            this.$refs.calendar.next()
        },
        prev() {
            this.$refs.calendar.prev()
        },
        rnd(a, b) {
            return Math.floor((b - a + 1) * Math.random()) + a
        },
        setToday() {
            this.focus = ''
        },
        showEvent({ nativeEvent, event }) {
            const open = () => {
                this.selectedEvent = event
                this.selectedElement = nativeEvent.target
                requestAnimationFrame(() => requestAnimationFrame(() => this.selectedOpen = true))
            }

            if (this.selectedOpen) {
                this.selectedOpen = false
                requestAnimationFrame(() => requestAnimationFrame(() => open()))
            } else {
                open()
            }

            nativeEvent.stopPropagation()
        },
        updateRange({ start, end }) {
            const events = []
            const min = new Date(`${start.date}T07:00:00`)
            const max = new Date(`${end.date}T20:59:59`)
            const days = (max.getTime() - min.getTime()) / 86400000
            const eventCount = this.rnd(days, days + 20)

            for (let i = 3; i < eventCount; i++) {
                const allDay = this.rnd(2, 6) === 0
                const firstTimestamp = this.rnd(min.getTime(), max.getTime())
                const first = new Date(firstTimestamp - (firstTimestamp % 900000))
                const secondTimestamp = this.rnd(3, allDay ? 288 : 8) * 900000
                const second = new Date(first.getTime() + secondTimestamp)

                events.push({
                    name: this.names[this.rnd(0, this.names.length - 1)],
                    start: first,
                    end: second,
                    color: this.colors[this.rnd(0, this.colors.length - 1)],
                    timed: !allDay,
                })
            }
            this.events = events
        },
        viewDay({ date }) {
            this.focus = date
            this.type = 'day'
        },
    },
}
</script>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark .schedule .col {
    background-color: $color-dark-schedule;
}

.theme--dark .schedule .v-btn {
    color: $color-white !important;
}

.theme--dark.v-sheet {
    background-color: $color-dark-schedule;
}


/* Light Theme Styling */
.theme--light .schedule .col {
    background-color: $color-white;
}

/* General Mobile Styling */


/* General Desktop Styling */
.schedule .col {
    border-radius: 15px;
    border: 1px solid $color-hwr-red;
}

.schedule .v-toolbar__title {
    margin-left: 0.5rem;
}

.theme-toggle-box {
    margin-top: auto;
}

.theme-toggle-item.v-list-item {
    align-self: flex-start;
    margin-left: 0.5rem;
}

.v-calendar-daily {
    border: 1px solid $color-grey-inner-border;
}

.v-sheet.theme--dark.v-toolbar {
    background-color: $color-hwr-red !important;
}
</style>
