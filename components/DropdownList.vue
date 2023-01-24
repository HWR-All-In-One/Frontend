<template>
  <div @click="selectNode" class="menu-item">
    <v-treeview :items="items"></v-treeview>

  </div>
</template>

<script>
export default {
  data: () => ({
    active: false,
    items: [
      {
        id: 10000,
        name: 'Fachrichtung',
        children: [
          { id: 20000, 
            name: 'Informatik', 
            children: [
              {
                id: 30000,
                name: 'Jahrgang',
                children: [
                  { 
                    id: 40000,
                    name: '2021',
                    children: [
                      {
                        id: 50000,
                        name: '1. Semester',
                        children: [
                          {
                            id: 60000, 
                            name: 'Kurs A',
                            link:'#'
                          },
                          {
                            id: 60001, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50001,
                        name: '2. Semester',
                        children: [
                          {
                            id: 60002, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60003, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50002,
                        name: '3. Semester',
                        children: [
                          {
                            id: 60004, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60005, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50003,
                        name: '4. Semester',
                        children: [
                          {
                            id: 60006, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60007, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50004,
                        name: '5. Semester',
                        children: [
                          {
                            id: 60008, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60009, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50005,
                        name: '6. Semester',
                        children: [
                          {
                            id: 60010, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60011,
                            name: 'Kurs B',
                          },
                        ],
                      },
                    ]  
                  },
                  { 
                    id: 40001, 
                    name: '2022',
                    children: [
                      {
                        id: 50006,
                        name: '1. Semester',
                        children: [
                          {
                            id: 60012, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60013, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50007,
                        name: '2. Semester',
                        children: [
                          {
                            id: 60014, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60015, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50008,
                        name: '3. Semester',
                        children: [
                          {
                            id: 60016, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60017, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50009,
                        name: '4. Semester',
                        children: [
                          {
                            id: 60018, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60019, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50010,
                        name: '5. Semester',
                        children: [
                          {
                            id: 60020, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60021, 
                            name: 'Kurs B',
                          },
                        ],
                      },
                      {
                        id: 50011,
                        name: '6. Semester',
                        children: [
                          {
                            id: 60022, 
                            name: 'Kurs A',
                          },
                          {
                            id: 60023,
                            name: 'Kurs B',
                          },
                        ],
                      },
                    ] 
                  },
                  { 
                    id: 40002, 
                    name: '2023' 
                  },
                ],
              },
            ],
          },     
        ]
      },
    ],
  }),
}
</script>

<style>
.menu-item {
  display: flex;
  color: #FFF;
  transition: 0.4s;
}
.v-treeview-node__root {
  display: flex;
  flex-direction: row;
  border: 1px solid #FFF;
}
.v-treeview-node__children {
  align-items: right;
}
</style>