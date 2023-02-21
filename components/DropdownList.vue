<template>
    <v-treeview selectable :items="items" @onclick="onSelected"/>
</template>

<script>
/**
 * Wir benötigen insgesamt eine Haupt und 5 Unterebenen bzw. untergegliederte Dropdowns
 * 
 * Fachrichtung (nicht klickbar - nur hover opening) [1. Ebene - Hauptebene]
 *  -> Informatik (nicht klickbar - nur hover opening) [2. Ebene - 1. Subebene]
 *      -> Jahrgang (nicht klickbar - nur hover opening) [3. Ebene - 2. Subebene]
 *          -> 2021 (nicht klickbar - nur hover opening) [4. Ebene - 3. Subebene]
 *              -> 1. Semester (nicht klickbar - nur hover opening) [5. Ebene - 4. Subebene]
 *                  -> Kurs A (klickbar - lädt den entsprechenden Kalender in die Webseite) [6. Ebene - 5. Subebene]
 *                  -> Kurs B (klickbar - lädt den entsprechenden Kalender in die Webseite)
 *                  -> Kurs C (klickbar - lädt den entsprechenden Kalender in die Webseite)
 *              -> 2. Semester (nicht klickbar - nur hover opening)
 *                  -> Kurs A (klickbar - lädt den entsprechenden Kalender in die Webseite)
 *                  -> Kurs B (klickbar - lädt den entsprechenden Kalender in die Webseite)
 *                  -> Kurs C (klickbar - lädt den entsprechenden Kalender in die Webseite)
 *              -> 3. Semester (nicht klickbar - nur hover opening)
 *              -> 4. Semester (nicht klickbar - nur hover opening)
 *              -> 5. Semester (nicht klickbar - nur hover opening)
 *              -> 6. Semester (nicht klickbar - nur hover opening)
 *              -> 7. Semester (nicht klickbar - nur hover opening)
 *          -> 2022 (nicht klickbar - nur hover opening)
 *          -> 2023 (nicht klickbar - nur hover opening)
 *  -> Maschinenebau
 */

export default {
    data: () => ({
        active: false,
        items: [
            {
                id: 10000,
                name: "Fachrichtung",
                children: [
                    {
                        id: 20000,
                        name: "Informatik",
                        children: [
                            {
                                id: 30000,
                                name: "Jahrgang",
                                children: [
                                    {
                                        id: 40000,
                                        name: "2021",
                                        children: [
                                            {
                                                id: 50000,
                                                name: "1. Semester",
                                                children: [
                                                    {
                                                        id: 60000,
                                                        name: "Kurs A",
                                                        link: "#"
                                                    },
                                                    {
                                                        id: 60001,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50001,
                                                name: "2. Semester",
                                                children: [
                                                    {
                                                        id: 60002,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60003,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50002,
                                                name: "3. Semester",
                                                children: [
                                                    {
                                                        id: 60004,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60005,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50003,
                                                name: "4. Semester",
                                                children: [
                                                    {
                                                        id: 60006,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60007,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50004,
                                                name: "5. Semester",
                                                children: [
                                                    {
                                                        id: 60008,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60009,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50005,
                                                name: "6. Semester",
                                                children: [
                                                    {
                                                        id: 60010,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60011,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    {
                                        id: 40001,
                                        name: "2022",
                                        children: [
                                            {
                                                id: 50006,
                                                name: "1. Semester",
                                                children: [
                                                    {
                                                        id: 60012,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60013,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50007,
                                                name: "2. Semester",
                                                children: [
                                                    {
                                                        id: 60014,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60015,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50008,
                                                name: "3. Semester",
                                                children: [
                                                    {
                                                        id: 60016,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60017,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50009,
                                                name: "4. Semester",
                                                children: [
                                                    {
                                                        id: 60018,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60019,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50010,
                                                name: "5. Semester",
                                                children: [
                                                    {
                                                        id: 60020,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60021,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                id: 50011,
                                                name: "6. Semester",
                                                children: [
                                                    {
                                                        id: 60022,
                                                        name: "Kurs A"
                                                    },
                                                    {
                                                        id: 60023,
                                                        name: "Kurs B"
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    {
                                        id: 40002,
                                        name: "2023"
                                    }
                                ]
                            }
                        ]
                    }
                ]
            }
        ]
    })
};
</script>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark.v-treeview {
    color: #000;
}

/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.menu-item {
    display: flex;
    color: $color-dark-mode-grey;
    transition: 0.4s;
}

.v-treeview-node__root {
    display: flex;
    flex-direction: row;
    border: 1px solid $color-hwr-red;
}

.v-treeview-node__children {
    align-items: right;
}
</style>
