<template>
  <div @click="selectNode" class="menu-item"  >
    <v-treeview :items="items"></v-treeview>

  </div>
</template>

<script>
  
  export default {
    data: () => ({
      active: false,
      items: [
        {
          id: 1 ,
          name: 'Fachrichtung',
          children: [
            { id: 2, name: 'Bank'},
            { id: 3, name: 'Bauwesen', 
            children: [
                {
                  id: 4,
                  name: 'Semester',
                  children: [
                    { id: 5,
                      name: '1 - Kurs A ',
                      children: [
                                  {
                                    id: 11,
                                    name: 'src :',
                                    children: [
                                      { id: 12, name: 'v-btn : ts' },
                                      { id: 13, name: 'v-card : ts' },
                                      { id: 14, name: 'v-window : ts' },
                                    ],
                                  },
                                ]  
                              },
                    { id: 6, name: '1 - Kurs B' },
                    { id: 7, name: '2 - Kurs A' },
                    { id: 8, name: '2 - Kurs B' },
                    { id: 9, name: '3 - Kurs A' },
                    { id: 10, name: '3 - Kurs B' },
                    { id: 11, name: '4 - Kurs A' },
                    { id: 12, name: '4 - Kurs B' },
                    { id: 13, name: '5 - Kurs A' },
                    { id: 14, name: '5 - Kurs B' },
                    { id: 13, name: '6 - Kurs A' },
                    { id: 14, name: '6 - Kurs B' },

                  ],
                },
              ],
            },
            { id: 15, name: 'DL' },
            { id: 16, name: 'Elektrotechnik' },
            { id: 17, name: 'FM' },
            { id: 18, name: 'Handel' },
            { id: 19, name: 'Iba' },
            { id: 20, name: 'Immobilien' },
            { id: 21, name: 'Industrie' },
            { id: 22, name: 'Informatik' },
            { id: 23, name: 'Wirtschaft Informatik' }       
          ]
        },
      ],
    }),
  }
  
</script>

<style>
.v-treeview-node__children{
align-items: center;
justify-content: center;
top: calc(100% + 18px);
width: max-content;

}

.menu-item
 {
  color: #FFF;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;
  transition: 0.4s;
}

</style>