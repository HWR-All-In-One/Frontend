<template>
  <div>
    <v-list class="dropdownlist">
      <list-item v-for="item in items" :item="item" :key="item.title">
      </list-item>
    </v-list>
  </div>
</template>

<script>
export default {
  name: "DashboardCoreDrawer",
  components: {
    ListItem: () => import("./listitem.vue")
  },
  data: () => ({
    items: [
            {
                
                title: "Fachrichtung",
                items: [
                    {
                        
                        title: "Informatik",
                        items: [
                            {
                                
                                title: "Jahrgang",
                                items: [
                                    {
                                        
                                        title: "2021",
                                        items: [
                                            {
                                                
                                                title: "1. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "2. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "3. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "4. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "5. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "6. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    {
                                        
                                        title: "2022",
                                        items: [
                                            {
                                                
                                                title: "1. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "2. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "3. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "4. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "5. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "6. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    {
                                        
                                        title: "2023",
                                        items: [
                                            {
                                                
                                                title: "1. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "2. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "3. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "4. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "5. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "6. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        to: "/account",
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B",
                                                        to: "/login",
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                ]
                            }
                        ]
                    },
                    {
                        
                        title: "Wirtschaft Informatik",
                        items: [
                            {
                                
                                title: "Jahrgang",
                                items: [
                                    {
                                        
                                        title: "2021",
                                        items: [
                                            {
                                                
                                                title: "1. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A",
                                                        link: "#"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "2. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "3. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "4. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "5. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "6. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    {
                                        
                                        title: "2022",
                                        items: [
                                            {
                                                
                                                title: "1. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "2. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "3. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "4. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "5. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "6. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    {
                                        
                                        title: "2023",
                                        items: [
                                            {
                                                
                                                title: "1. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "2. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "3. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "4. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "5. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            },
                                            {
                                                
                                                title: "6. Semester",
                                                items: [
                                                    {
                                                        
                                                        title: "Kurs A"
                                                    },
                                                    {
                                                        
                                                        title: "Kurs B"
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                ]
                            }
                        ]
                    },
                ]
            }
        ]
  })
};
</script>